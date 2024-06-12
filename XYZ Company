#Variable Initialization
choice=0
project_code=[]
client_name=[]
start_date=[]
expected_end_date=[]
number_of_workers=[]
project_status=[]
p_code=0
c_name=0
begining_date=0
end_date=0
num_workers=0
p_status=0
ongoing=0
completed=0
onhold=0
available_workers=1000
result=0
actual_end_date=[]
completed_p=[]
onhold_p=[]
ongoing_p=[]



            




#Display the main menu

while True:
    print("__________________________________________________________________________________________________________")
    print()
    print(" ::::::::::::::::::::::: ********************* :::::::::::::::::::::::")
    print(" ::::::::::::::::::::::: *    XYZ Company    * :::::::::::::::::::::::")
    print(" ::::::::::::::::::::::: *    Main Menu      * :::::::::::::::::::::::")
    print(" ::::::::::::::::::::::: ********************* :::::::::::::::::::::::")
    print()
    1==print("1. Add a new project to existing projects. ")
    2==print("2. Remove a completed project from existing projects. ")
    3==print("3. Add new workers to available workers group. ")
    4==print("4. Update details on ongoing projects. ")
    5==print("5. Project Statistics ")
    6==print("6. Exit ")
    
    print()
#Get the choice from the user
    choice=int(input("                                                                       Your Choice: "))
    print("__________________________________________________________________________________________________________")
    print()
    #If the user enters the choice 1, display the add a new project details
    if choice==1:
        
        
        print(" ::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print(" ::::::::::::::::::::::: *    XYZ Company     * :::::::::::::::::::::::")
        print(" ::::::::::::::::::::::: *  Add a new project * :::::::::::::::::::::::")
        print(" ::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print()
        print()
        p_code=int(input("Project Code                        -   (**Enter '0' to Project code to exit)       "))

        #Get the inputs from the user about the client's details
        if p_code in project_code:
            print()
            print("This project already exists.")
            print()
        else:
            x=0
            while x<5:
                if p_code==0:
                    print()                     
                    print(" You exited from the Add a new project interface. ")
                    print(" Enter 6 as choice to exit from the whole interface. ")
                    print("                 Thank You!                          ")
                          
                    break
                
                
                else:
                    c_name=str(input("Clent's Name                        -    "))
                    begining_date=str(input("Start date        (DD-MM-YYYY)      -    "))
                    end_date=str(input("Expected end date (DD-MM-YYYY)      -    "))
                    num_workers=int(input("Number of workers                   -    "))
                    p_status=str(input("Project status (ongoing,onhold)     -    "))
                    if p_status=="onhold":
                        if num_workers>available_workers:
                            print()
                            print("Not enough number of workers.")
                            project_code.append(p_code)
                            client_name.append(c_name)
                            start_date.append(begining_date)
                            expected_end_date.append(end_date)
                            number_of_workers.append(num_workers)
                            project_status.append(p_status)
                            
                    
                            onhold=onhold+1
                            
                            print("The Project is added to onhold projects.")
                            print()
                            onhold_p.append(p_code)
                            onhold_p.append(c_name)
                            onhold_p.append(begining_date)
                            onhold_p.append(end_date)
                            onhold_p.append(num_workers)
                            onhold_p.append(p_status)
                            break
                        else:
                            print()
                            print("There are enough number of workers to begin the project.")
                            print("Please change the project status as ongoing.")
                            print()
                            print("Re-enter the details again.")
                            print()
                            break
                            
                    elif p_status=="completed":
                        print()
                        print("Completed projects cannot be added.")
                        print()
                        break
                    
                    elif p_status=="ongoing":
                    
                    
                        #Check the availability of workers
                        if num_workers>available_workers:
                            print()
                            print("Not enough number of workers.")
                            print("Please change the project status as onhold.")
                            print()
                            break
            
                        else:
                            ans=str(input("Do you want to save the project(Yes/No):"))
                            #Append the inputs to the list
                            if ans=="Yes":
                                available_workers=available_workers-num_workers
                                ongoing=ongoing+1
                                print()
                                project_code.append(p_code)
                                client_name.append(c_name)
                                start_date.append(begining_date)
                                expected_end_date.append(end_date)
                                number_of_workers.append(num_workers)
                                project_status.append(p_status)
                                #print(project_code)
                                #print(client_name)
                                #print(start_date)
                                #print(expected_end_date)
                                #print(number_of_workers)
                                #print(project_status)
                                print()
                                print("The project is successfully added.")
                                print()
                                break
                            else:
                                print()
                                print("The project is not added.")
                                print()
                                break
                    else:
                        print()
                        print("Invalid project status.")
                        print()
                        break
        
            
                           
    
    #If the user enters the choice 1, display remove completed project details  
        
    elif choice==2:
        print("::::::::::::::::::::::: ***************************** :::::::::::::::::::::::")
        print("::::::::::::::::::::::: *    XYZ Company            * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: * Remove Completed Project  * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: ***************************** :::::::::::::::::::::::")
        print()
        print()
        p_code=int(input("Project Code    -    "))
        
        #Check whether the project is available in the list
        
        if p_code in project_code:
            index=project_code.index(p_code)
            workers=number_of_workers[index]
            status=project_status[index]
            
            if status=="ongoing":
                print()
                print("Ongoing projects cannot be removed.")
                print("This project should be completed to remove.")
                print()
                  
            elif status=="onhold":
                print()
                print("Onhold projects cannot be removed. ")
                print("This project should be completed to remove.")
                print()
                
            elif status=="completed":        
                    
                print()
                ans=input("Do you want to remove the project(Yes/No)?   ")
                #Pop details needed to be removed from the project
                if ans=="Yes":
                    
                    project_code.pop(index)
                    client_name.pop(index)
                    start_date.pop(index)
                    expected_end_date.pop(index)
                    number_of_workers.pop(index)
                    project_status.pop(index)
                    
                    #print(project_code)
                    #print(client_name)
                    #print(start_date)
                    #print(expected_end_date)
                    #print(number_of_workers)
                    #print(project_status)
                    print()
                    print("Project is removed successfully.")
                    print()
                else:
                    print()
                    print("The project is not removed.")
                    print()
            
        else:
            print()
            print("The project is not existing.")
            print()
        
        
       


            
                  
                
        



    
     #If the user enters the choice 3, display add new workers setup.
    elif choice==3:
        print("::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print("::::::::::::::::::::::: *    XYZ Company     * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: * Add new workers    * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print()
        print()
        new_workers=int(input("Number workers to add  -  "))
        ans=input("Do you want to add(Yes/No)? ")

        #Add new workers to the variable
        if ans=="Yes":
            available_workers+=new_workers
            #print(available_workers)
            print()
            print("New workers are added successfully")
            print()
        elif ans=="No":
            print()
            print("New workers were not added")
            print()
        else:
            print()
            print("Invalid input")
            print()
        
     
     #If the user enters the choice 4, display update project details setup.
    elif choice==4:
        print("::::::::::::::::::::::: *************************** :::::::::::::::::::::::")
        print("::::::::::::::::::::::: *    XYZ Company          * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: * Update Project Details  * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: *************************** :::::::::::::::::::::::")
        print()
        print()
        p_code=int(input("Project Code                                      -    "))
        x=0
        #Input the project details needed to be updated.
        while x<5:
            if p_code==0:
                print()                     
                print(" You exited from the Add a new project interface. ")
                print(" Enter 6 as choice to exit from the whole interface. ")
                print("                 Thank You!                          ")
                break
            else:
                if p_code not in project_code:
                    print()
                    print("Invalid code")
                    break
                else:
                    index=project_code.index(p_code)
                    workers=number_of_workers[index]
                    status=project_status[index]
                    c_name=str(input("Clent's Name                                      -    "))
                    begining_date=str(input("Start date         (DD-MM-YYYY)                   -    "))
                    end_date=str(input("Expected end date  (DD-MM-YYYY)                   -    "))
                    num_workers=int(input("Number of workers                                 -    "))
                    
                    
                    
                
                    #Check the availability of workers.
                    if num_workers!=workers:
                        result=num_workers-workers
                        if result>0 and result>available_workers:
                            print()
                            print("Sorry number of workers are not sufficient")
                            print()
                            break
                        else:
                            p_status=str(input("Project status (ongoing,onhold,completed)         -    "))
                            print()
                            ans=input("Do you want to update the project data(Yes/No)?   -    ")
                            if ans!="Yes":
                                break
                            else:
                                client_name[index]=c_name
                                start_date[index]=begining_date
                                expected_end_date[index]=end_date
                                if result>0 and result<available_workers:
                                    
                                    number_of_workers[index]=num_workers
                                    
                                    project_status[index]=p_status
   
                                    if status!=p_status:
                                        if p_status=="completed":
                                            ac_date=str(input    ("Actual end date   (DD-MM-YYYY)                    -    "))
                                            completed_p.append(p_code)
                                            completed_p.append(c_name)
                                            completed_p.append(begining_date)
                                            completed_p.append(end_date)
                                            completed_p.append(ac_date)
                                            completed_p.append(num_workers)
                                            completed_p.append(p_status)
                                            ongoing=ongoing-1
                                            completed=completed+1
                                            available_workers=available_workers+num_workers
                                            print()
                                            print("The project is updated successfully.")
                                            #print(completed)
                                            break
                                        elif p_status=="onhold":
                                            print()
                                            hold_date=str(input  ("Date of the hold                                  -  "))
                                            hold_reason=str(input("Reason for holding the project                    -  "))
                                            onhold_p.append(p_code)
                                            onhold_p.append(c_name)
                                            onhold_p.append(begining_date)
                                            onhold_p.append(end_date)
                                            onhold_p.append(hold_date)
                                            onhold_p.append(hold_reason)
                                            onhold_p.append(num_workers)
                                            onhold_p.append(p_status)
                                            
                                            onhold=onhold+1
                                            ongoing=ongoing-1
                                            available_workers=available_workers+num_workers
                                            print()
                                            print("The project is updated successfully.")
                                            print()
                                            break
                                        elif p_status=="ongoing":
                                                ongoing=ongoing+1
                                                available_workers=available_workers-num_workers
                                                ongoing_p.append(p_code)
                                                ongoing_p.append(c_name)
                                                ongoing_p.append(begining_date)
                                                ongoing_p.append(end_date)
                                                ongoing_p.append(num_workers)
                                                ongoing_p.append(p_status)
                                                
                                                #print(project_status)
                                                #print(ongoing)
                                                #print(onhold)
                                                #print(completed)
                                                #print(completed_p)
                                                #print(onhold_p)
                                                print()
                                                print("The project is updated successfully.")
                                                break
                                        else:
                                            print()
                                            print("Invalid project status")
                                            print()
                                            break
                                    
                                    else:
                                        print()
                                        print("The project status is same as previous")
                                        print()
                                        break
                                else:
                                
                                    
                                    number_of_workers[index]=num_workers
                                    
                                    project_status[index]=p_status
       
                                    if status!=p_status:
                                        if p_status=="completed":
                                            ac_date=str(input    ("Actual end date   (DD-MM-YYYY)                    -    "))
                                            completed_p.append(p_code)
                                            completed_p.append(c_name)
                                            completed_p.append(begining_date)
                                            completed_p.append(end_date)
                                            completed_p.append(ac_date)
                                            completed_p.append(num_workers)
                                            completed_p.append(p_status)
                                            ongoing=ongoing-1
                                            completed=completed+1
                                            available_workers=available_workers+num_workers
                                            #print(completed_p)
                                            print()
                                            print("The project is updated successfully.")
                                            print()
                                            break
                                            
                                        elif p_status=="onhold":
                                            hold_date=str(input  ("Date of the hold                                  -  "))
                                            hold_reason=str(input("Reason for holding the project                    -  "))
                                            onhold_p.append(p_code)
                                            onhold_p.append(c_name)
                                            onhold_p.append(begining_date)
                                            onhold_p.append(end_date)
                                            onhold_p.append(hold_date)
                                            onhold_p.append(hold_reason)
                                            onhold_p.append(num_workers)
                                            onhold_p.append(p_status)
                                                
                                            onhold=onhold+1
                                            ongoing=ongoing-1
                                            available_workers=available_workers+num_workers
                                            print()
                                            print("The project is updated successfully.")
                                            print()
                                            break
                                        else:
                                            if p_status=="ongoing":
                                                ongoing=ongoing+1
                                                available_workers=available_workers-num_workers
                                                ongoing_p.append(p_code)
                                                ongoing_p.append(c_name)
                                                ongoing_p.append(begining_date)
                                                ongoing_p.append(end_date)
                                                ongoing_p.append(num_workers)
                                                ongoing_p.append(p_status)
                                                print()
                                                print("The project is updated successfully.")
                                                print()
                                                
                                                break
                                    else:
                                        print()
                                        print("Invalid Project status")
                                        print()
                                        break

                            
                                                
                                    
                    else:
                        p_status=str(input("Project status (ongoing,onhold,completed)         -    "))
                        print()
                        ans=input("Do you want to update the project data(Yes/No)?   -    ")
                        if ans=="Yes":
                            
                            number_of_workers[index]=num_workers
                            project_status[index]=p_status
                            
                            if status!=p_status:
                                if p_status=="completed":
                                    ac_date=str(input    ("Actual end date   (DD-MM-YYYY)                    -    "))
                                    completed_p.append(p_code)
                                    completed_p.append(c_name)
                                    completed_p.append(begining_date)
                                    completed_p.append(end_date)
                                    completed_p.append(ac_date)
                                    completed_p.append(num_workers)
                                    completed_p.append(p_status)
                                    ongoing=ongoing-1
                                    completed=completed+1
                                    available_workers=available_workers+num_workers
                                    print()
                                    print("The project is updated successfully.")
                                    print()
                                    break
                                elif p_status=="onhold":
                                    hold_date=str(input  ("Date of the hold                                  -  "))
                                    hold_reason=str(input("Reason for holding the project                    -  "))
                                    onhold_p.append(p_code)
                                    onhold_p.append(c_name)
                                    onhold_p.append(begining_date)
                                    onhold_p.append(end_date)
                                    onhold_p.append(hold_date)
                                    onhold_p.append(hold_reason)
                                    onhold_p.append(num_workers)
                                    onhold_p.append(p_status)
                                    
                                    onhold=onhold+1
                                    ongoing=ongoing-1
                                    available_workers=available_workers+num_workers
                                    print()
                                    print("The project is updated successfully.")
                                    print()
                                        
                                    #print(project_status)
                                    #print(ongoing)
                                    #print(onhold)
                                    #print(completed)
                                    break
                                else:
                                    if p_status=="ongoing":
                                        ongoing=ongoing+1
                                        available_workers=available_workers-num_workers
                                        ongoing_p.append(p_code)
                                        ongoing_p.append(c_name)
                                        ongoing_p.append(begining_date)
                                        ongoing_p.append(end_date)
                                        ongoing_p.append(num_workers)
                                        ongoing_p.append(p_status)
                                        print()
                                        print("The project is updated successfully.")
                                        print()
                                        break
                            else:
                                print()
                                print("The project details are same as the previous")
                                print("No update in the details")
                                break
                        else:
                            print()
                            print("The project is not updated")
                            break
                             
                                           
       

                    
        
     #If the user enters the choice 5, display project statistics setup.  
    elif choice==5:
        print("::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print("::::::::::::::::::::::: *    XYZ Company     * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: * Project Statistis  * :::::::::::::::::::::::")
        print("::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
        print()
        print()
        print("Number of ongoing projects            -      ",ongoing)
        print("Number of completed projects          -      ",completed)
        print("Number of on hold projects            -      ",onhold)
        print("Number of available workers to assign -    ",available_workers)

        print()
        ans=str(input("Do you want to add the project(Yes/No)?   "))
        print()
        

        if ans=="Yes":
            print(" ::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
            print(" ::::::::::::::::::::::: *    XYZ Company     * :::::::::::::::::::::::")
            print(" ::::::::::::::::::::::: *  Add a new project * :::::::::::::::::::::::")
            print(" ::::::::::::::::::::::: ********************** :::::::::::::::::::::::")
            print()
            print()
            p_code=int(input("Project Code                        -   (**Enter '0' to Project code to exit)  "))
            #Get the inputs from the user about the client's details
            p_code 
            if p_code in project_code:
                print()
                print("This project already exists")
                print()
            else:
                x=0
                while x<5:
                    if p_code==0:
                        print()
                        break
                    else:
                        c_name=str(input("Clent's Name                        -    "))
                        begining_date=str(input("Start date        (DD-MM-YYYY)      -    "))
                        end_date=str(input("Expected end date (DD-MM-YYYY)      -    "))
                        num_workers=int(input("Number of workers                   -    "))
                        p_status=str(input("Project status (ongoing,onhold)     -    "))
                        if p_status=="onhold":
                            if num_workers>available_workers:
                                print("Not enough number of workers")
                                print()
                        
                                onhold=onhold+1
                                print("The Project is added to onhold projects")
                                onhold_p.append(p_code)
                                onhold_p.append(c_name)
                                onhold_p.append(begining_date)
                                onhold_p.append(end_date)
                                onhold_p.append(num_workers)
                                onhold_p.append(p_status)
                                break
                        elif p_status=="completed":
                            print()
                            print("Completed projects cannot be added")
                            print()
                            break
                        
                        elif p_status=="ongoing":
                        
                        
                            #Check the availability of workers
                            if num_workers>available_workers:
                                print()
                                print("Not enough number of workers")
                                print("Please change the project status as onhold")
                                print()
                                break
                
                            else:
                                ans=str(input("Do you want to save the project(Yes/No):"))
                                #Append the inputs to the list
                                if ans=="Yes":
                                    available_workers=available_workers-num_workers
                                    ongoing=ongoing+1
                                    print()
                                    project_code.append(p_code)
                                    client_name.append(c_name)
                                    start_date.append(begining_date)
                                    expected_end_date.append(end_date)
                                    number_of_workers.append(num_workers)
                                    project_status.append(p_status)
                                    #print(project_code)
                                    #print(client_name)
                                    #print(start_date)
                                    #print(expected_end_date)
                                    #print(number_of_workers)
                                    #print(project_status)
                                    print()
                                    print("Project is successfully added")
                                    print()
                                    break
                                else:
                                    print()
                                    print("New project is not added")
                                    print()

        elif ans=="No":
           print()
           print("New project is not added.")
           print()
           
        else:
            print()
            print("Invalid input")
            print()
            
     #If the user enters the choice 6, display exit.   
    elif choice==6:
        print()
        print("                                  *******************************                                              ")                     
        print("                                  *****        Exit.       ******                                              ")
        print("                                  *****      Thank You!    ******                                              ")
        print("                                  *******************************                                              ")
        print()
        print("__________________________________________________________________________________________________________")
        
        break
    else:
        print()
        print("Invalid choice")
        print("Please try again.")
