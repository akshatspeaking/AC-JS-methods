## Array Method Practice

### Open `index.html` and do the following in the script tag
- 1. Write a function called `countAllPeople` which counts the total number of people in `got` variable defined in `data.js` file.

function countAllPeople(got) {

return got.houses.reduce(function (acc, val){

val.people.map(x => {
  let name = x.name;
  acc.push(name);
})
return acc;

}, []).length;

}

- 2. Write a function called `peopleByHouses` which counts the total number of people in different houses in the `got` variable defined in `data.js` file.

function peopleByHouses(got) {
got.houses.map(house => {

    return (house.name + " " + house.people.length);
   })
};


USING REDUCE:
got.houses.reduce((acc, cv) => {return acc + cv.people.length}, 0);

- 3. Write a function called `everyone` which returns a array of names of all the people in `got` variable.

function everyone(got) {

 return got.houses.reduce(function (acc, val){

   val.people.forEach(x => {
   acc.push(x.name);
})
return acc
}, []);

}


- 4. Write a function called `nameWithS` which returns a array of names of all the people in `got` variable whose name includes `s` or `S`.

function nameWithS (got) {
   let names = everyone(got);
   let ans = [];
   for (name of names) {
      if (name.includes("s") || name.includes("S")) {
         ans.push(name);
      }
   }
   return ans;
}

USING REDUCE:

got.houses.reduce((acc, cv) => {
cv.people.forEach(x => {
	if(x.name.includes("s") || (x.name.includes("S"))) {
	acc.push(x.name);
}
})
return acc;
}, [])


}, [])


- 5. Write a function called `nameWithA` which returns a array of names of all the people in `got` variable whose name includes `a` or `A`.

function nameWithA (got) {
   let names = everyone(got);
   let ans = [];
   for (name of names) {
      if (name.includes("a") || name.includes("A")) {
         ans.push(name);
      }
   }
   return ans;
}

USING REDUCE:
got.houses.reduce((acc, cv) => {
cv.people.forEach(x => {
	if(x.name.includes("a") || (x.name.includes("A"))) {
	acc.push(x.name);
}
})
return acc;
}, [])

- 6. Write a function called `surnameWithS` which returns a array of names of all the people in `got` variable whoes surname is starting with `S`(capital s).

function surnameWithS (got) {
   let names = everyone(got);
   let surnames = names.map(name => name.split(" ")[1])
   let ans = [];
   for (surname of surnames) {
      if (surname.startsWith("S")) {
         ans.push(surname);
      }
   }
   return ans;
}

USING REDUCE:

got.houses.reduce((acc, cv) => {
cv.people.forEach(x => {
	if(x.name.includes("s") || (x.name.includes("S"))) {
	acc.push(x.name);
}
})
return acc;
}, [])

- 7. Write a function called `surnameWithA` which returns a array of names of all the people in `got` variable whoes surname is starting with `A`(capital a).

function surnameWithA (got) {
   let names = everyone(got);
   let surnames = names.map(name => name.split(" ")[1])
   let ans = [];
   for (surname of surnames) {
      if (surname.startsWith("A")) {
         ans.push(surname);
      }
   }
   return ans;
}

USING REDUCE:

got.houses.reduce((acc, cv) => {
cv.people.forEach(x => {
	if(x.name.split(" ")[1].startsWith("A")) {
	acc.push(x.name);
}
});
return acc;
}, []);

- 8. Write a function called `everyone` which returns a array of names of all the people in `got` variable.

same as 3

- 9. Solve all the above functions with `reduce` array method. Make different method for all.





