https://github.com/SUContent/SFT-Regular-Exam.git

cd C:\Users\DESI\Desktop\SFT-Regular-Exam
dir
notepad run-concatenation-fourth.js

function runConcatenation() {
    function concatenateTextAndNumbers(text, numbers) {
        var sortedText = text.split('').sort().join(''); // Rearrange the letters in alphabetical order
        var sortedNumbers = numbers.sort(function(a, b) { return b - a; }); // Rearrange the numbers in descending order
        var result = sortedText + " ";
        for (var i = 0; i < sortedNumbers.length; i++) {
            result += sortedNumbers[i].toString();
            if (i !== sortedNumbers.length - 1) {
                result += ", ";
            }
        }
        return result;
    }

    var args = process.argv.slice(2);
    var text = args[0];
    var numbers = args.slice(1).map(Number);

    console.log(concatenateTextAndNumbers('We are expecting the new Indiana Jones film soon', [100, 200]));
}

runConcatenation();
__________________________________________________________________

 IJWaaacdeeeeeeefghiiilmnnnnnnoooprssttwx 200, 100


