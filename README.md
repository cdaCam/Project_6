# Project_6 UML Class Diagram


In the layout of the classes for easier read

classDiagram
    class MainFrame {
        - WelcomePanel welcomePanel         
        - PizzaPanel pizzaPanel            
        - ToppingsPanel toppingsPanel       
        - DrinksPanel drinksPanel           
        + MainFrame()                       
        + createButtonPanel()               
    }

    class WelcomePanel {
        - JLabel welcomeLabel              
        + WelcomePanel()                 
    }

    class PizzaPanel {
        - JRadioButton thinCrust           
        - JRadioButton thickCrust          
        - ButtonGroup pizzaGroup            
        + PizzaPanel()                     
        + getBaseCost() double             
    }


    class ToppingsPanel {
        - JCheckBox cheese             
        - JCheckBox pepperoni               
        - JCheckBox pineapple              
        - JCheckBox goldFlakes            
        + ToppingsPanel()                  
        + getToppingCost() double           
    }

    class DrinksPanel {
        - JRadioButton coke                 
        - JRadioButton dietCoke           
        - JRadioButton sweetTea            
        - ButtonGroup drinksGroup           
        - JSpinner drinkQuantitySpinner    
        + DrinksPanel()                    
        + getDrinkCost() double            
    }

    MainFrame --> WelcomePanel : "contains"
    MainFrame --> PizzaPanel : "contains"
    MainFrame --> ToppingsPanel : "contains"
    MainFrame --> DrinksPanel : "contains"
