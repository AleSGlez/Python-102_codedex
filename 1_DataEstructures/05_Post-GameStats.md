# 🏁 05. Post-Game Stats - Chapter Wrap-Up

### 📚 What You Learned:
- Basic data types: `int`, `float`, `str`, `bool`
- **Tuples** → ordered and immutable sequences
- **Dictionaries** → unordered key-value pairs
- **Sets** → unordered collections of unique items

---

## 🧠 Quick Refresher
```python
# Tuple
teams = ('TeamA', 'TeamB')

# Dictionary
basketball_player = {'name': 'LeBron James', 'team': 'Los Angeles Lakers'}

# Set
soccer_positions = {'Forward', 'Midfielder', 'Defender', 'Goalkeeper'}
```

---

## 📊 Final Exercise: Data Structures in Action
You’re a data analyst for a sports team. Let’s practice applying data structures to real-world data!

```python
#Create a list of dictionaries where each dictionary represents a player
players_data = [
  {'name': 'Jude Bellingham', 'position': 'midfielder', 'jersey_num':5, 'matches': 31, 'goals': 9},
  {'name': 'Arda Güler', 'position': 'midfielder', 'jersey_num':15, 'matches': 28, 'goals': 3},
  {'name': 'Antonio Rüdiger', 'position': 'defender', 'jersey_num':22, 'matches': 29, 'goals': 0},
  {'name': 'Federico Valverde', 'position': 'midfielder', 'jersey_num':8, 'matches': 36, 'goals': 6},
]

names = [player["name"] for player in players_data]
print("Players Names:", names)

#Print out a list of all player positions in the dataset.
positions = [player["position"]for player in players_data]
print("Players Position", positions)

#Choose a player and update their game statistics in the dataset.
players_data[2]["goals"] += 2


#Calculate the average statistics for all players and print the results.
average_goals = sum(player["goals"] for player in players_data) / len(players_data)
average_matches = sum(player["matches"] for player in players_data) / len (players_data)
print("Average Goals Scored: ", average_goals)
print("Average Matches: ", average_matches)culate the average** of one or more statistics across all players and print the results.
```

Output
```python
Players Names: ['Jude Bellingham', 'Arda Güler', 'Antonio Rüdiger', 'Federico Valverde']
Players Position ['midfielder', 'midfielder', 'defender', 'midfielder']
Average Goals Scored:  5.0
Average Matches:  31.0
```



![image](https://github.com/user-attachments/assets/1f6b77a4-4c63-4e74-b61c-af50e7774da0)
