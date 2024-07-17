# IPL-Dashboard-using-MS-Excel-

Load the dataset to provide an overview.

import pandas as pd

# Load the dataset
file_path = '/mnt/data/IPL_Dataset.xlsx'
xls = pd.ExcelFile(file_path)

# List all sheet names to understand the structure
sheet_names = xls.sheet_names
sheet_names

Result
['Sheet1']

The dataset contains a single sheet named "Sheet1." Let's take a look at the first few rows of this sheet to understand its structure and contents.

# Load the first sheet into a DataFrame
df = pd.read_excel(xls, sheet_name='Sheet1')

# Display the first few rows of the dataset
df.head()

# Result
   id       city    Season       date player_of_match  \
0   1  Hyderabad  IPL-2017 2017-04-05    Yuvraj Singh   
1   2       Pune  IPL-2017 2017-04-06       SPD Smith   
2   3     Rajkot  IPL-2017 2017-04-07         CA Lynn   
3   4     Indore  IPL-2017 2017-04-08      GJ Maxwell   
4   5  Bangalore  IPL-2017 2017-04-08       KM Jadhav   

                                       venue                        team1  \
0  Rajiv Gandhi International Stadium, Uppal          Sunrisers Hyderabad   
1    Maharashtra Cricket Association Stadium               Mumbai Indians   
2     Saurashtra Cricket Association Stadium                Gujarat Lions   
3                     Holkar Cricket Stadium       Rising Pune Supergiant   
4                      M Chinnaswamy Stadium  Royal Challengers Bangalore   

                         team2                  toss_winner toss_decision  \
0  Royal Challengers Bangalore  Royal Challengers Bangalore         field   
1       Rising Pune Supergiant       Rising Pune Supergiant         field   
2        Kolkata Knight Riders        Kolkata Knight Riders         field   
3              Kings XI Punjab              Kings XI Punjab         field   
4             Delhi Daredevils  Royal Challengers Bangalore           bat   

   result                       winner  win_by_runs  win_by_wickets  \
0  normal          Sunrisers Hyderabad           35               0   
1  normal       Rising Pune Supergiant            0               7   
2  normal        Kolkata Knight Riders            0              10   
3  normal              Kings XI Punjab            0               6   
4  normal  Royal Challengers Bangalore           15               0   

          umpire1        umpire2  
0     AY Dandekar       NJ Llong  
1  A Nand Kishore         S Ravi  
2     Nitin Menon      CK Nandan  
3    AK Chaudhary  C Shamshuddin  
4             NaN            NaN  

Here is a preview of your IPL dataset, with the following columns:

- `id`: Match identifier
- `city`: City where the match was played
- `Season`: IPL season year
- `date`: Date of the match
- `player_of_match`: Player awarded as the man of the match
- `venue`: Venue of the match
- `team1`: Team 1
- `team2`: Team 2
- `toss_winner`: Team that won the toss
- `toss_decision`: Decision made by the toss winner (bat/field)
- `result`: Result type (normal/tie/no result)
- `winner`: Winning team
- `win_by_runs`: Runs by which the team won
- `win_by_wickets`: Wickets by which the team won
- `umpire1`: First umpire
- `umpire2`: Second umpire

# IPL Dataset

This repository contains a dataset of Indian Premier League (IPL) matches. The data covers various aspects of the matches, including the date, venue, teams, toss decisions, match results, and more.

## Dataset Description

The dataset includes the following columns:

- **id**: Unique identifier for each match.
- **city**: The city where the match was played.
- **Season**: The IPL season year.
- **date**: The date on which the match was played.
- **player_of_match**: The player who was awarded the man of the match.
- **venue**: The venue where the match was held.
- **team1**: The first team playing the match.
- **team2**: The second team playing the match.
- **toss_winner**: The team that won the toss.
- **toss_decision**: The decision made by the toss-winning team (either to bat or field).
- **result**: The result type of the match (e.g., normal, tie, no result).
- **winner**: The team that won the match.
- **win_by_runs**: The number of runs by which the team won the match.
- **win_by_wickets**: The number of wickets by which the team won the match.
- **umpire1**: The first umpire of the match.
- **umpire2**: The second umpire of the match.

## Usage

This dataset can be used for various data analysis and machine learning tasks, such as:

- Analyzing team performance over different seasons.
- Identifying factors that contribute to a team's victory.
- Predicting match outcomes based on historical data.
- Visualizing trends and patterns in IPL matches.

## How to Use

1. Clone the repository to your local machine:
   
    git clone https://github.com/yourusername/IPL_Dataset.git

2. Navigate to the repository directory:
   
    cd IPL_Dataset

3. Load the dataset in your preferred data analysis tool (e.g., Python, R):
    import pandas as pd

    df = pd.read_excel('IPL_Dataset.xlsx')

## License

This dataset is provided for educational and research purposes. Please attribute the source when using this dataset.

## Contributing

If you have any suggestions or improvements, feel free to submit a pull request or open an issue.

You can customize this template further based on your specific needs. Let me know if you need any additional information or modifications!
