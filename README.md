# full-satrk-home-work
function sortArrayDescending(arr) {
    for (let i = 0; i < arr.length - 1; i++) {
        for (let j = i + 1; j < arr.length; j++) {
            if (arr[i] < arr[j]) {
                let temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
    return arr;
}
console.log(sortArrayDescending([5, 2, 9, 1, 5])); // [9,5,5,2,1]

function commonValues(arr1, arr2) {
    let result = [];
    for (let i = 0; i < arr1.length; i++) {
        for (let j = 0; j < arr2.length; j++) {
            if (arr1[i] === arr2[j]) {
                if (!result.some(val => val === arr1[i])) {
                    result.push(arr1[i]);
                }
                break;
            }
        }
    }
    return result;
}
console.log(commonValues([1, 2, 1, 2, 1], [2, 2, 2, 1, 3, 1, 2])); // [1,2]

function averageMatrix(matrix) {
    let sum = 0;
    let count = 0;
    for (let i = 0; i < matrix.length; i++) {
        for (let j = 0; j < matrix[i].length; j++) {
            sum += matrix[i][j];
            count++;
        }
    }
    return sum / count;
}
console.log(averageMatrix([[1, 2, 3], [4, 5, 6]])); // 35

function countAndRemove(arr, num) {
    let count = 0;
    for (let i = arr.length - 1; i >= 0; i--) {
        if (arr[i] === num) {
            arr.pop();
            count++;
        }
    }
    return count;
}
let arr = [1, 2, 3, 2, 4, 2];
console.log(countAndRemove(arr, 2)); // 3
console.log(arr); // [1,2,3]

const isStringLongerThanFive = str => str.length > 5;
console.log(isStringLongerThanFive("hello")); // false
console.log(isStringLongerThanFive("helloworld")); // true

const isFirstAndLastSame = str => {
    if (str[0] === str[str.length - 1]) {
        return "The first and last characters are the same.";
    } else {
        return "The first and last characters are different.";
    }
};
console.log(isFirstAndLastSame("hello")); // "different"
console.log(isFirstAndLastSame("radar")); // "same"

const isLastCharacterUppercase = str =>
    str[str.length - 1] >= 'A' && str[str.length - 1] <= 'Z' ? true : false;
console.log(isLastCharacterUppercase("hellO")); // true
console.log(isLastCharacterUppercase("hello")); // falce

function checkDivisibleBy3(arr) {
    let found = false;
    arr.forEach((num, index) => {
        if (num % 3 === 0) {
            console.log(Number ($)+{num} ("at index") + {$index});
            found = true;
        }
    });
    if (!found) {
        console.log("The array is not divisible by 3");
    }
}
checkDivisibleBy3([2, 5, 6, 7, 9, 11, 12, 1]); 
// Number 6 at index 2
// Number 9 at index 4
// Number 12 at index 6
checkDivisibleBy3([1, 4, 5, 7]); 
// "The array is not divisible by 3"

function checkUpperCaseLowerCase(arr) {
    const result = [];
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === arr[i].toUpperCase()) {
            result.push("U"); // אות גדולה
        } else {
            result.push("L"); // אות קטנה
        }
    }
    return result;
}

console.log(checkUpperCaseLowerCase(["A", "B", "c", "d", "E"])); // ["U", "U", "L", "L", "U"]

function replaceEvenIndex(arr) {
    const result = [];
    for (let i = 0; i < arr.length; i++) {
        if (i % 2 === 0) {
            result.push(i);
        } else {
            result.push(arr[i]);
        }
    }
    return result;
}

const inputArray = ["a", "b", "c", "d", "e", "f"];
console.log(replaceEvenIndex(inputArray)); // [0, "b", 2, "d", 4, "f"]

function filterAgesOver18(ages) {
    return ages.filter(age => age > 18);
}
const ages = [12, 18, 25, 30, 17, 20];
console.log(filterAgesOver18(ages)); // [25, 30, 20]

function removeIndex3(arr) {
    return arr.filter((_, index) => index !== 3);
}
const array = [2, 4, 1, 2, 7, 2, 8];
console.log(removeIndex3(array)); // [2, 4, 1, 7, 2, 8]

const names = ["Alice", "Bob", "Charlie"];

function addNameToArray(newName) {
    names.push(newName);
    return names;
}
console.log(addNameToArray("Diana")); // ["Alice", "Bob", "Charlie", "Diana"]

function mergeNameArrays(array1, array2) {
    return [...array1, ...array2];
}
const names1 = ["Alice", "Bob"];
const names2 = ["Charlie", "Diana"];
console.log(mergeNameArrays(names1, names2)); // ["Alice", "Bob", "Charlie", "Diana"]
