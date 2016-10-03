nielsen x edward - filter to show unique names

js -

// original provided array with duplicate names
var duplicatesArray = ['Nick', 'jake', 'RAY', 'Kate', 'Nick', 'Jeremy', 'nick', 'AMOL', 'rAY', 'VIANNEY', 'Shilpika', 'nick', 'THOMAS', 'tom', 'james', 'JERM', 'amOl', 'kate', 'SCOTT', 'Jenifer', 'bill', 'jenny', 'STEVEN']

// loop through duplicatesArray, lowercase all characters, remove duplicates
for(i = 0; i < duplicatesArray.length; i++) {
	var i = duplicatesArray.indexOf(duplicatesArray[i])
	if(i != -1) {
		duplicatesArray.splice(i, 1)
	}
}
// print to console
console.log(duplicatesArray)

// jquery onclick button to write to document
	$('#click').on('click',function() {

	// jquery append marking for styling
	$('.unique').append('[')
		
		// for loop through each item of uniqueArray, append for styling
		for (var i=0; i<duplicatesArray.length;i++){
			$('.unique').append("'" + duplicatesArray[i] +"', ")
			}

		// jquery append marking for styling
	$('.unique').append(']')
})
// end onlick, write to document
