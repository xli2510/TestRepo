df = pd.read_csv("data/PRECIP_HLY_sample_csv.csv")
df.head()
df = df.drop(columns=["STATION", "ELEVATION"], errors="ignore")
