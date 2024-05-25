# 🐶 DogShelterApp
 Dog shelter management app, providing two application modes: admin and user mode.
 
 - Admin Mode - used to manage and visualize the dogs from the shelter. Basic CRUD
operations are provided.

- User Mode - used to present dogs for the user to adopt, tracking the adopted dogs in an adoption list. 
The adoption list can be stored in HTML or CSV format.

## Used Concepts and Several Application Features
- Graphical User Interface, built using the ```QT Framework```
- Layered Architecture: ```presentation layer``` (application UI), ```business layer``` (application service), ```persistence layer``` (application repositories)
- Usage of OOP concepts such as ```inheritance```, ```encapsulation```, ```polymorphism``` and ```abstraction```. One such example of ```inheritance``` and ```polymorphism``` usage: in the application's persistence layer, I've defined a polymorphic class called *Repository*, which contains virtual methods for adding, deleting, and updating dog records. There are derived classes such as *FileRepository*, *CSVRepository*, and *HTMLRepository*, all of which inherit from the base *Repository* class to provide their own specific implementations.The decision regarding which format to use is made dynamically, depending on the user's choice. The application's service maintains a reference to a *Repository* object, which will actually hold the address of a *CSVRepository* or of a *HTMLRepository* object, depending on the user's preference.
- Usage of QT signals and slots
- Exceptions handling

## Design Patterns Used
- ```Model-View-Controller``` for displaying the adoption list in the table, the photos being shown using QT delegates
- ```Command``` design pattern, used for the undo/redo functionality

## Other Application Features
- Letting the user select the application mode (```user``` or ```admin```) and, if ```user``` is chosen, what type of adoption list is wanted (```CSV``` or ```HTML```) at launch.
- Undo and Redo functionality for the features related to managing dogs and adopting dogs. These also work with the usual key combinations (```CTRL - Z``` and ```CTRL - Y```).

## Project Screenshots
 ### Choose the application mode window:
 <p align="center"> <img src="https://github.com/AndreiGota/DogShelterApp/blob/main/Project%20Screenshots/Screenshot%20204223.png" height="500"/> </p>

 ### Admin mode window:
 <p align="center"> <img src="https://github.com/AndreiGota/DogShelterApp/blob/main/Project%20Screenshots/Screenshot%20204527.png" height="500"/> </p>

 ### User mode window
  <p align="center"> <img src="https://github.com/AndreiGota/DogShelterApp/blob/main/Project%20Screenshots/Screenshot%20204854.png" height="500"/> </p>

 ### Adoption list displayed externally, in ```HTML``` format in this case:
  <p align="center"> <img src="https://github.com/AndreiGota/DogShelterApp/blob/main/Project%20Screenshots/Screenshot%20205203.png" height="300"/> </p>
 
 
