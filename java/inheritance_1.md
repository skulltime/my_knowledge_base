// Design a Java program to model a Vehicle  hierarchy.   

//     Create a superclass Vehicle with attributes speed and color, and a method displayInfo().  
//     Implement single inheritance  by creating a subclass Car that inherits from Vehicle and adds a model attribute. Override displayInfo() to include the model.  
//     Implement multilevel inheritance  by creating a subclass SportsCar that inherits from Car and adds a turbo attribute. Override displayInfo() again.  
//     Use super to call the superclass constructor and methods.

'''
 class Vehicle{
    int speed;
    String color;
    Vehicle(int speed, String color){ 
        this.speed = speed;
        this.color = color;
    }
    void displayInfo(){
        System.out.println("The speed is " + speed + " The color is " + color); 
    }
}
class Car extends Vehicle {
    String model;
    Car(int speed, String color , String model){
        super(speed,color);
        this.model = model;
    }
    
  void displayInfo(){
        // super.displayInfo(); 
        System.out.println("The speed is " + speed + " The color is " + color); 
        System.out.println("The Model of the car is: " + model);
    }
}
class SportsCar extends Car{
    int turbo; //idk what turbo means 
    SportsCar(int speed,String color, String model,int turbo){
        super(speed,color,model);
            this.turbo = turbo;
        
  }
    
  void displayInfo(){
        // super.displayInfo();
        System.out.println("The speed is " + speed + " The color is " + color); 
        System.out.println("The Model of the car is: " + model);
        System.out.println("The turbo of the car is: " + turbo);
    }
		
public static void main(String[] args) {
        SportsCar s = new SportsCar(300,"Blue","Ferrari 89G",98);
        s.displayInfo();
        Vehicle n = new Vehicle(100, "black");
        n.displayInfo();
        System.out.println("\nspeed of the car is "+n.speed);
    }
}
'''
