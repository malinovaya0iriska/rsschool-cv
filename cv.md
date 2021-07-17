# CV #
## IRYNA MARTSULEVICH ##
### Front-end developer ( Junior ) ###
### About me ###
***
 I am a novice developer with experience in creating SPAs using _JavaScript, TypeScript, React, Redux._ 
 My goal is to become a full-stack developer. 
 Ability to work in a team and constant self-study, no problem finding common ground with people, also work well in a team. 
 I spend my free time learning _English_ with my tutor and _technical documentation._

### Education ###
***
* Vitebsk State Order Of Peoples’ Friendship Medical University 2016,General Medicine Faculty, Anaesthetist
*  It-incubator
*  Udemi
*  W3school
*  Lectures CS50
*  HTML-Academy
*  Books: 
   *  Javascript For Kids
   *  Head First HTML with CSS

   ### English Level ###
***
* B1-B2(Intermediate/Upper-Intermediate)

### Code example  ###
***
    export type StateType = {
    id: string
    title: string
    isDone: boolean
  }
   export type FilterValuesType = 'all' | 'active' | 'completed'

   export const App = () => {
    const [tasks, setTasks] = useState<Array<StateType>>(
        [
            {id: v1(), title: 'HTML&CSS', isDone: true},
            {id: v1(), title: 'JS', isDone: false},
            {id: v1(), title: 'React', isDone: false},
            {id: v1(), title: 'Typescript', isDone: true}
        ])

    let [filter, setFilter] = useState<FilterValuesType>('all')
    let filteredTasks = tasks
    if (filter === 'active') {
        filteredTasks = tasks.filter(t => t.isDone === false)
    }
    if (filter === 'completed') {
        filteredTasks = tasks.filter(t => t.isDone === true)
    }
    const filterTask = (value: FilterValuesType) => {
        setFilter(value)
    }

    const removeTask = (taskID: string) => {
        const restTasks = tasks.filter(t => t.id !== taskID)
        setTasks(restTasks)
    }

    const addTask = (gotTitle: string) => {
        const newTask = {id: v1(), title: gotTitle, isDone: false}
        setTasks([newTask, ...tasks])
    }

    const setCheckBox = (taskID: string, isDone: boolean) => {
        const checkedTask = tasks.find(t => taskID === t.id)
        if (checkedTask) {
            checkedTask.isDone = isDone
            setTasks([...tasks])
        }
    }
    return (
        <div className="App">
            <TodoList title={'What to learn'}
                      tasks={filteredTasks}
                      removeTask={removeTask}
                      filterTask={filterTask}
                      addTask={addTask}
                      filter={filter}
                      setCheckBox={setCheckBox}/>
        </div>
    );
}

### SKILLS: ###
***
* HTML5;
* CSS3;
* Git;
* JS;
* TypeScript;
* React;
* GitHub;
* TDD/UNIT Tests;
* Storybook;
