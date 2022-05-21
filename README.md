#include <iostream>
#include <conio.h>
#include <string.h>
#include <string>
#include <fstream>
#include<stdlib.h>// funcione new y delete
#include <vector>

using namespace std;

struct DIENTES{
    string nom1;
    string citahorario;
    string tratamiento;
    string descripcion;
    int tot;
};

//definir la funcion
void Alta();
void listas();
void archivos();
void eliminar();
void modificar();

int alta, * matricula, * calf, * calflab, * subtotal, * iva, * total;
string horam1;
string horam2;
string horam3;
string horam4;
string horam5;
string horam6;
int sehorario = 0;
string* nombre;

DIENTES datos[3];

int excion = 150;
int trat = 0;
int ncita = 0;
int dent = 350;
int endo = 400;
int esca = 580;
int hdes = 0;

int i;
int j = 0;
int k = 0;
int l = 0;
int m = 0;
int p = 0;


int main()
{
    
    int op;
    string horam1;
    string horam2;
    string horam3;
    string horam4;
    string horam5;
    string horam6;
    int sehorario = 0;
   
    double ho0 = true;
    double ho2 = true;
    double ho4 = true;
    double ho6 = true;
    double ho8 = true;
    double ho10 = true;
    double ho12 = true;
    double ho14 = true;
    double ho16 = true;
    double ho18 = true;
    double ho20 = true;
    double ho22 = true;
    double ho24 = true;
    cout << "Bienvenido a la Clinica Dental" << endl << "1) Agendar cita" << endl << "2) Mostrar cita" << endl << "3) Limpiar Pantalla" << endl << "4) Modificar Cita" << endl << "5) Eliminar Cita" << endl << "6) Salir" << endl;
    cin >> op;
    switch (op)
    {
    case 1:
        Alta();
                
                return main();
                break;
    case 2:
        listas();
        return main();
        break;
    case 3:
        system("cls"); //system("clear");
        return main();
        break;
    case 4:
        modificar();
        return main();
    case 5:
        eliminar();
        return main();
        break;
    case 6:
        return 0;
        break;
    default:
        cout << "Ingrese una opcion valida";
            }

        }
        void Alta()
        {
            cout << "Digite el numero de citas que desea dar de alta" << endl;
            cin >> alta;
            matricula = new int[alta]; //arreglos
            calf = new int[alta];
            calflab = new int[alta];
            nombre = new string[alta];
            for (int i = 0; i < alta; i++)
            {
                cout << "Ingrese matricula" << endl; //printf
                cin >> matricula[i]; //scanf %d
                while (getchar() != '\n'); //se vacia el buffer o el espacio o cin.ignore
                cout << "Ingrese su nombre" << endl;
                getline(cin, nombre[i]); //permite los espacios en el nombre


                cout << "Seleccione un horario disponible para su cita" << endl;
                cout << "0 -- 4 -- 8" << endl << "12 -- 16 -- 20" << endl;
                cin >> sehorario;
                if (sehorario == 0)
                {
                    if (horam1 == "12 AM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 12 AM" << endl;
                        horam1 = "12 AM";
                        datos[j].citahorario = "12 AM";
                    }
                }
                if (sehorario == 4)
                {
                    if (horam2 == "4 AM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 4 AM" << endl;
                        horam2 = "4 AM";
                        datos[j].citahorario = "4 AM";
                    }
                }
                if (sehorario == 8)
                {
                    if (horam3 == "8 AM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 8 AM" << endl;
                        horam3 = "8 AM";
                        datos[j].citahorario = "8 AM";
                    }
                }
                if (sehorario == 12)
                {
                    if (horam4 == "12 PM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 12 PM" << endl;
                        horam4 = "12 PM";
                        datos[j].citahorario = "12 PM";
                    }
                }
                if (sehorario == 16)
                {
                    if (horam5 == "4 PM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 4 PM" << endl;
                        horam5 = "4 PM";
                        datos[j].citahorario = "4 PM";
                    }
                }
                if (sehorario == 20)
                {
                    if (horam6 == "8 PM")
                    {
                        cout << "Este horario ya esta ocupado" << endl;
                    }
                    else
                    {
                        cout << "Su cita fue asignada a las 8 PM" << endl;
                        horam6 = "8 PM";
                        datos[j].citahorario = "8 PM";
                    }
                }

                cout << "Escoja uno de los siguientes tratamientos" << endl << "1) Dentadura parcial" << endl << "2) Endodoncias" << endl << "3) Escalado y Alisado Radicular" << endl << "4) Extraccion";
                cout << endl;
                cin >> hdes;
                if (hdes == 1)
                {
                    cout << "Si le faltan uno o mas dientes, puede notar la diferencia a la hora de masticar y hablar. Los puentes pueden ayudarle a recuperar la sonrisa. Un puente, que también se denomina dentadura parcial fija, sustituye los dientes que faltan con dientes artificiales y literalmente salva el espacio en el que antes habia uno o mas dientes." << endl << "El precio unitario del tratamiento es de $350 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * dent;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Dentadura parcial" << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Dentadura parcial";
                        datos[p].descripcion = "Si le faltan uno o mas dientes, puede notar la diferencia a la hora de masticar y hablar. Los puentes pueden ayudarle a recuperar la sonrisa. Un puente, que también se denomina dentadura parcial fija, sustituye los dientes que faltan con dientes artificiales y literalmente salva el espacio en el que antes habia uno o mas dientes.";
                  
                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 2)
                {
                    cout << "Si tiene un diente o una muela seriamente dañada, picada o una infeccion dental seria, su dentista podria recomendarle un tratamiento endodontico. Las endodoncias se utilizan para reparar y salvar su diente o muela en vez de extraerla." << endl << "El precio unitario del tratamiento es de $400 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * endo;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Endodoncias." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Endodoncias";
                        datos[p].descripcion = "Si tiene un diente o una muela seriamente dañada, picada o una infeccion dental seria, su dentista podria recomendarle un tratamiento endodontico. Las endodoncias se utilizan para reparar y salvar su diente o muela en vez de extraerla.";
                        
                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 3)
                {
                    cout << "Se le podra aplicar una tecnica odontologica para tratamiento de enfermedades periodontales. Es importante recalcar que esta tecnica implica la limpieza profunda de las raices de los dientes.." << endl << "El precio unitario del tratamiento es de $580 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * esca;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Escalado y Alisado Radicular." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Escalado y Alisado Radicular";
                        datos[p].descripcion = "Se le podra aplicar una tecnica odontologica para tratamiento de enfermedades periodontales. Es importante recalcar que esta tecnica implica la limpieza profunda de las raices de los dientes.";
                        
                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 4)
                {
                    cout << "Una extraccion significa quitar un diente, por lo general a causa de alguna enfermedad o traumatismo o porque hay dientes amontonados." << endl << "El precio unitario del tratamiento es de $150 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * excion;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Extraccion." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Extraccion";
                        datos [p].descripcion = "Una extraccion significa quitar un diente, por lo general a causa de alguna enfermedad o traumatismo o porque hay dientes amontonados.";

                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                k = k + 1;


            }
        }

        void listas()
        {
            for (int i = 0; i < alta; i++)
            {
                if (matricula[i] == 0)
                {
                    cout << "CITA ELIMINADA" << i + 1 << endl;
                }
                else
                {
                    cout << " Cita" << i + 1 << endl;
                    cout << matricula[i] << endl;
                    cout << nombre[i] << endl;
                    cout << datos[i].citahorario << endl;
                    cout << datos[i].tratamiento << endl;
                    cout << datos[i].descripcion << endl;
                    cout << datos[i].tot << endl;
                }
            }
        }

        void modificar()
        {
            int j, opcion;
            cout << "ingrese el numero registro a modificar";
            cin >> j;
            j = j - 1; // esto debido a que i inicia en 0
            cout << "ingrese que desea modificar 1.-Matricula,2.-Nombre, 3.-Horario, 4.-Tratamiento" << endl;
            cin >> opcion;

            switch (opcion)
            {
            case 1:
                for (int i = j; i == j; i++)
                {
                    cout << "Ingrese matricula" << endl;
                    cin >> matricula[i];
                }
                break;
            case 2:
                for (int i = j; i == j; i++)
                {
                    while (getchar() != '\n'); //se vacia el buffer o el espacio
                    cout << "Ingrese nombre" << endl;
                    getline(cin, nombre[i]);
                }
                break;

            case 3:
                for (int i = j; i == j; i++)
                {
                    cout << "Ingrese su horario" << endl;
                    cout << "Seleccione un horario disponible para su cita" << endl;
                    cout << "0 -- 4 -- 8" << endl << "12 -- 16 -- 20" << endl;
                    cin >> sehorario;
                    if (sehorario == 0)
                    {
                        if (horam1 == "12 AM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 12 AM" << endl;
                            horam1 = "12 AM";
                            datos[j].citahorario = "12 AM";
                        }
                    }
                    if (sehorario == 4)
                    {
                        if (horam2 == "4 AM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 4 AM" << endl;
                            horam2 = "4 AM";
                            datos[j].citahorario = "4 AM";
                        }
                    }
                    if (sehorario == 8)
                    {
                        if (horam3 == "8 AM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 8 AM" << endl;
                            horam3 = "8 AM";
                            datos[j].citahorario = "8 AM";
                        }
                    }
                    if (sehorario == 12)
                    {
                        if (horam4 == "12 PM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 12 PM" << endl;
                            horam4 = "12 PM";
                            datos[j].citahorario = "12 PM";
                        }
                    }
                    if (sehorario == 16)
                    {
                        if (horam5 == "4 PM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 4 PM" << endl;
                            horam5 = "4 PM";
                            datos[j].citahorario = "4 PM";
                        }
                    }
                    if (sehorario == 20)
                    {
                        if (horam6 == "8 PM")
                        {
                            cout << "Este horario ya esta ocupado" << endl;
                        }
                        else
                        {
                            cout << "Su cita fue asignada a las 8 PM" << endl;
                            horam6 = "8 PM";
                            datos[j].citahorario = "8 PM";
                        }
                    }
                    

                }
            case 4:
                cout << "Escoja uno de los siguientes tratamientos" << endl << "1) Dentadura parcial" << endl << "2) Endodoncias" << endl << "3) Escalado y Alisado Radicular" << endl << "4) Extraccion";
                cout << endl;
                cin >> hdes;
                if (hdes == 1)
                {
                    cout << "Si le faltan uno o mas dientes, puede notar la diferencia a la hora de masticar y hablar. Los puentes pueden ayudarle a recuperar la sonrisa. Un puente, que también se denomina dentadura parcial fija, sustituye los dientes que faltan con dientes artificiales y literalmente salva el espacio en el que antes habia uno o mas dientes." << endl << "El precio unitario del tratamiento es de $350 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * dent;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Dentadura parcial" << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Dentadura parcial";
                        datos[p].descripcion = "Si le faltan uno o mas dientes, puede notar la diferencia a la hora de masticar y hablar. Los puentes pueden ayudarle a recuperar la sonrisa. Un puente, que también se denomina dentadura parcial fija, sustituye los dientes que faltan con dientes artificiales y literalmente salva el espacio en el que antes habia uno o mas dientes.";

                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 2)
                {
                    cout << "Si tiene un diente o una muela seriamente dañada, picada o una infeccion dental seria, su dentista podria recomendarle un tratamiento endodontico. Las endodoncias se utilizan para reparar y salvar su diente o muela en vez de extraerla." << endl << "El precio unitario del tratamiento es de $400 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * endo;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Endodoncias." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Endodoncias";
                        datos[p].descripcion = "Si tiene un diente o una muela seriamente dañada, picada o una infeccion dental seria, su dentista podria recomendarle un tratamiento endodontico. Las endodoncias se utilizan para reparar y salvar su diente o muela en vez de extraerla.";

                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 3)
                {
                    cout << "Se le podra aplicar una tecnica odontologica para tratamiento de enfermedades periodontales. Es importante recalcar que esta tecnica implica la limpieza profunda de las raices de los dientes.." << endl << "El precio unitario del tratamiento es de $580 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * esca;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Escalado y Alisado Radicular." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Escalado y Alisado Radicular";
                        datos[p].descripcion = "Se le podra aplicar una tecnica odontologica para tratamiento de enfermedades periodontales. Es importante recalcar que esta tecnica implica la limpieza profunda de las raices de los dientes.";

                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                if (hdes == 4)
                {
                    cout << "Una extraccion significa quitar un diente, por lo general a causa de alguna enfermedad o traumatismo o porque hay dientes amontonados." << endl << "El precio unitario del tratamiento es de $150 ¿Desea ingresar al tratamiento?" << endl << "1) Si" << endl << "2) No";
                    cout << endl;
                    cin >> hdes;
                    if (hdes == 1)
                    {
                        cout << "¿Cuantas sesiones le gustaria tomar? Entre mas sean mejor seran sus dientes" << endl;
                        cin >> trat;
                        datos[m].tot = trat * excion;
                        ncita = ncita + 1;
                        cout << "#" << ncita << " de cita. " << datos[k].nom1 << " tiene una cita a las " << datos[j].citahorario << ". Su tratamiento es Extraccion." << endl << "Tendra un total de " << trat << " sesiones, lo cual sera un costo de $" << datos[m].tot;
                        j = j + 1;
                        datos[l].tratamiento = "Extraccion";
                        datos[p].descripcion = "Una extraccion significa quitar un diente, por lo general a causa de alguna enfermedad o traumatismo o porque hay dientes amontonados.";

                        l = l + 1;
                        m = m + 1;
                        p = p + 1;
                    }
                    else
                    {
                        if (hdes == 2)
                        {
                            cout << "Elija otro tratamiento";
                        }
                        else
                        {
                            cout << "Ingrese un numero valido";
                        }
                    }
                }
                k = k + 1;
                
                break;
            }


        }

        void eliminar()
        {
            int j;
            cout << "ingrese la cita a eliminar";
            cin >> j;
            j = j - 1;
            for (int i = j; i == j; i++)
            {
                cout << "Eliminando cita" << j + 1 << endl;

                matricula[i] = 0;
                nombre[i] = " ";
                datos[i].citahorario = "";
                datos[i].tratamiento = "";
                datos[i].tot = 0;
            }
        }
