# Matplotlib Cheat Sheet (Minimal & Clean)

## Importing Libraries

```python
import matplotlib.pyplot as plt
import numpy as np
```

## Creating Sample Data

```python
x = np.linspace(0, 10, 100)
y = np.sin(x)
```

## Basic Line Plot

```python
plt.plot(x, y)
plt.show()
```

## Scatter Plot

```python
plt.scatter(x, y)
plt.show()
```

## Bar Plot

```python
categories = ['A', 'B', 'C']
values = [10, 20, 15]
plt.bar(categories, values)
plt.show()
```

## Horizontal Bar Plot

```python
plt.barh(categories, values)
plt.show()
```

## Histogram

```python
data = np.random.randn(1000)
plt.hist(data, bins=30, color='skyblue', edgecolor='black')
plt.show()
```

## Pie Chart

```python
sizes = [30, 40, 30]
labels = ['A', 'B', 'C']
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.show()
```

## Subplots

```python
plt.figure(figsize=(10,4))

plt.subplot(1,2,1)
plt.plot(x, y)
plt.title('Line Plot')

plt.subplot(1,2,2)
plt.scatter(x, y)
plt.title('Scatter Plot')

plt.show()
```

## Customization

```python
plt.plot(x, y, color='red', linestyle='--', linewidth=2, marker='o')
plt.title('Customized Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.grid(True)
plt.show()
```

## Saving Figure

```python
plt.plot(x, y)
plt.savefig('figure.png', dpi=300)
plt.show()
```
