# AxessWrapper
A wrapper for axess 'vie scolaire'

Code will be released by the end of dev

## To-do and structure

class Axess : 

  params : 
  
    username : str : your username of connection
    
    password : str : your password
    
    verbose : bool : if you want logs to be shown in the terminal (default = True)
    
  vars : 
  
    verbose : bool : know if you want log to be print - done
    
    user_agents : list : a list of various user agent for increased discretion - done
    
    headers : dict : a predefined user agent to imitate a web browser - done
    
    urls : dict : contains all the necessary urls - done
    
    infos : dict : storing useful informations about the user (use getInformations) - done
    
    grades : dict : storing user's grades (use getGrades) - done
    
    homeworks : dict : sotring user's homework (use getHomeworks)
    
    study_planner : dict : storing the user's planner (use getStudyPlanner)
  
  methods : 
  
    _log(text : str) : to print 'text' in the terminal if verbose is enabled - done
    
    _connect(username : str,password : str) : initialize connexion (credentials are not stored !) - done
    
    getInformations() : replace self.infos with the current user informations - done
    
    getGrades() : replace self.grades with the current grade of th user - done
    
    getHomeworks() : replace self.homeworks with the homework of the user
    
    getStudyPlanner() : replace self.study_planner with the user's planner (this week and the following week)
    
    
