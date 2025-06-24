import matplotlib.pyplot as plt

# Data
age_groups = ['0 to 20 Years', '21 to 64 Years', '65+ Years']
population_millions = [512, 807, 98]
colors = ['gold', 'dodgerblue', 'deeppink']

# Create the bar chart
plt.figure(figsize=(10, 6))
bars = plt.bar(age_groups, population_millions, color=colors)

# Add value labels on top of bars
for bar in bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, yval + 10, f'{yval}M', ha='center', fontsize=12)

# Add title and axis labels
plt.title("India's Population Distribution by Age (2022)", fontsize=14)
plt.xlabel("Age Groups")
plt.ylabel("Population (in Millions)")
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.tight_layout()
plt.show()
