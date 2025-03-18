#include <iostream>
#include <string>
using namespace std;


struct PetroleumProduct {
    string name;
    int quantity;
    double price;
};

int main() {
    PetroleumProduct product;

    int choice;
    do {
        cout << "\nPetroleum Management System Menu:" << endl;
        cout << "1. Add Product" << endl;
        cout << "2. Display Product" << endl;
        cout << "3. Update Quantity" << endl;
        cout << "4. Update Price" << endl;
        cout << "5. Exit" << endl;
        cout << "Enter your choice: ";
        cin >> choice;

        switch(choice) {
            case 1:  
                cout << "Enter product name: ";
                cin >> product.name;
                cout << "Enter product quantity: ";
                cin >> product.quantity;
                cout << "Enter product price: ";
                cin >> product.price;
                cout << "Product added successfully!" << endl;
                break;
            
            case 2:  
                cout << "Product Name: " << product.name << endl;
                cout << "Quantity: " << product.quantity << endl;
                cout << "Price: $" << product.price << endl;
                break;

            case 3:  
                cout << "Enter new quantity: ";
                cin >> product.quantity;
                cout << "Quantity updated!" << endl;
                break;

            case 4:  
                cout << "Enter new price: ";
                cin >> product.price;
                cout << "Price updated!" << endl;
                break;

            case 5:  
                cout << "Exiting system..." << endl;
                break;

            default:
                cout << "Invalid choice. Please try again!" << endl;
        }
    } while (choice != 5);

    return 0;
}
