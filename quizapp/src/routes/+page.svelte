<script>
    import Question from '$lib/Question.svelte'
    import Answer from '$lib/Answer.svelte'
    import Points from '$lib/Points.svelte'

let points = 0
    let quizIndex = 0

    const quiz = [
        {
            question: "Is the Scarlet Witch a scarlet woman?",
            correctAnswer: 0,
            answers: [
                'Yes', 
                'No'
            ]
        },
        {
            question: "Is Cat Woman a bitch?",
            correctAnswer: 2,
            answers: [
                'Yes',
                'Maybe',
                'Robin Knows', 
                'No'
            ]
        }
    ]

    const checkAnswerHandler = (answerText) => {
        const Q = quiz[quizIndex]
        const isCorrect =  Q.answers.indexOf(answerText) == Q.correctAnswer
        if (isCorrect) {
            points+=1
            quiz[quizIndex].question = "Correct!"
        }
        else {
            quiz[quizIndex].question = `Wrong &#x1F622;`
        }
        setTimeout(()=> {quizIndex += 1},2000)
    }


</script>

<div class="App">
    <Points {points}/>
    <Question  questionText={quiz[quizIndex].question}/>
    <div class="btn-group">
        {#each quiz[quizIndex].answers as answerText, index }       
            <Answer {answerText} {checkAnswerHandler} />
        {/each}
    </div>
</div>
