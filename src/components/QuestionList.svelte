<script>
    import Question from './Question.svelte'
    import {
      Content,
      Grid,
      Row,
      Column,
    } from "carbon-components-svelte";
    let questions = [{
        id: '000001',
        q: 'What is the capital of India',
        opt: [{a:'Delhi',c: true,id:1},{a:'Kolkata',c:false,id:2}]
    },
    {
        id: '000002',
        q: 'What is the capital of Australia',
        opt: [{a:'Canberra',c: true,id:1},{a:'Melbourne',c:false,id:2}]
    }
    ]
     let questionnum
     
</script>

<Content>
    <Grid>
        {#each questions as question, questionnum}     
        <Row>
            <Column>
                    <Question {question} {questionnum}/>
         </Column> 
        </Row>
        {/each}
    </Grid>
</Content>
