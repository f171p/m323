3.1
```javascript
function sumList(numbers) {
    if (numbers.length === 0) return 0;
    return numbers[0] + sumList(numbers.slice(1));
}
```

3.2
```javascript
function averageList(numbers) {
    function helper(numbers, sum, count) {
        if (numbers.length === 0) return sum / count;
        return helper(numbers.slice(1), sum + numbers[0], count + 1);
    }
    return numbers.length === 0 ? 0 : helper(numbers, 0, 0);
}
```

3.3
```javascript
function sortStrings(strings) {
    if (strings.length <= 1) return strings;
    const [pivot, ...rest] = strings;
    return [
        ...sortStrings(rest.filter(s => s.localeCompare(pivot) < 0)),
        pivot,
        ...sortStrings(rest.filter(s => s.localeCompare(pivot) >= 0))
    ];
}
```

3.4
```javascript
function sortObjects(objects) {
    if (objects.length <= 1) return objects;
    const [pivot, ...rest] = objects;
    return [
        ...sortObjects(rest.filter(o => 
            o.date < pivot.date || 
            (o.date === pivot.date && o.priority < pivot.priority) || 
            (o.date === pivot.date && o.priority === pivot.priority && o.title.localeCompare(pivot.title) < 0)
        )),
        pivot,
        ...sortObjects(rest.filter(o => 
            o.date > pivot.date || 
            (o.date === pivot.date && o.priority > pivot.priority) || 
            (o.date === pivot.date && o.priority === pivot.priority && o.title.localeCompare(pivot.title) >= 0)
        ))
    ];
}
```

3.5
```javascript
function extractLeaves(tree) {
    if (!tree.children || tree.children.length === 0) return [tree.value];
    return tree.children.flatMap(extractLeaves);
}
```
