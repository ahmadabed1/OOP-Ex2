# OOP-Ex2
## This project has been developed as an assignment in OOP course.

# Pokemon game 
## what it is?
It's all about a Pokemon game.\
We got a graph with unlimited pokemons, and Specific number of agents.\
We need to locate the agent and run the game , the agents will collect the pokemons one by one, until the time end, every time the agent collect pokemon, other pokemon will appear on the graph.\
The basic idea is to get a high score, for that we need to collect more pokemons to get a high score, in that we need to locat the agent in correct location.


## About the project:-
this project splitted for two parts:
- in the first part , i have developed infrastructure for the game.
  which is depend on three basic interfaces , to get graph propreties.{ node_data, directed_weighted_graph, dw_graph_algorithms}

- in the second part , it is all about the pokemon game.
  it has the JFrame and the moving functions , which bulit using the first part.


* First part:
this part Specific to build graph propreties.
it has three basic interfces:
1. node_data :represents the set of operations applicable on a node (vertex) in a (directional) weighted graph contains a key, weight, info, tag.
2. directed_weighted_graph: represents a directional weighted graph ,has a road-system or communication network in mind ,it support a large number of nodes (over 100,000).it based on an efficient compact representation.
3. dw_graph_algorithms:  represents a Directed Weighted Graph Theory Algorithms contains copy, init, isConnected, shortestPathDist, List<node_data> shortestPath(int src, int dest), Save(file)-JSON file, Load(file)-JSON file.

* Secound part:
this part is to build the game.
it has many classes that every one of them complete the other classes to run the game,\
the class is :
1. Ex2: which build to start the game.
2. Ex2_Client: its has all the functions to build the game{ run, moveAgants, nextNode, distCal....) , and have the perpose operations to run the game, which it divide the action beetween other classes.
3. Arena : it's an helper class which save the the list of agent and pokemon and it locat them on the game map(in the Jframe).
4. MyFrame: it is the Jframe classs , its mission to Draw the game on our screen to see what going on the game.
	it also has a bar to help as play the game.
	in this bar we can choose which game scenarios we want to play with, olso we can save the graph, also it give the player option to run the game or stop it , also adding new agents.
	start Game option will be dependent on number of agent(which need to fill specefic num of agent in every game scenarios).
5. Cl_Agent: this class represent one agent player , it hold basic data on the agent , like its id , location , direction and speed.
6. Cl_Pokemon:this class represent one Pokemon player , it hold basic data on it, like its id , location and the edge that have it.



## How the game run:
the player need to choose the game scenarios , and locat the agent on it , and put start button , then the game will run autumaticlly.\
the movement of the agent to collect the pokemons based on dijkstra-algorithm(to find the shortestes path distance to the pokemons).\
also , the game has an timer for the end of the game , if the time up then the game will stop running and the score that the player got will be shown.



## how to play
at first you need to run the game , you have to option to run the game , you can use the jar file to run it , or run it by the basic way which is going to Ex2.java file and run it.\
![firstPic](https://user-images.githubusercontent.com/73795045/102718525-43fae600-42f1-11eb-95d8-e288c82c1c3e.png)

when the game start run, you will got a new game frame for the game , which has a bar to run the game , this bar give you those options:
- File: this menu for basic operation , which it has:
	1. Load game - menu item to choose which scenario to play with
	2. Save game - menu item to save the graph in json format
	3. exit - menu item to exit the game
- Game:
	1. start game - menu item to start/run the game
	2. stop game - menu item to stop/end the game 
	3. add agent - menu item to locat new agent on the graph

after chosen the game scenario and filling it's agents , you can run the game by choosing start game menu item.
the game will stop by choosing stop game menu item , or by time up, and the score that you have got will be showin in the consol.
you can choose other game scenario and play the game more and more.
if you want to exit the game you can put X button or by chosing  exit menu item.
