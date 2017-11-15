#include <iostream>
#include <cstdlib>
#include <ctime>

int main()
{
    srand( time( NULL ) );

    int zgaduj, wylosowana, i;
    wylosowana =(std::rand() % 1000) + 1;
    std::cout << "Wylosowalem liczbe od 1 do 1000. Zgadnij, jaka?" << std::endl;
    i=0;
    do
    {
        std::cin >> zgaduj;
        if (zgaduj > wylosowana)
        {
            std::cout << "Za duza!" << std::endl;
        }

        if (zgaduj < wylosowana)
        {
            std::cout << "Za mala!" << std::endl;
        }
        i++;

    }while (zgaduj != wylosowana);
    std::cout << "Gratulacje, trafiles! Liczba strzalow: " << i << std::endl;
    return 0;
}
