<script>
    //import { CodeSnippet } from "carbon-components-svelte";
    import {
    Form,
    FormGroup,
    RadioButtonGroup,
    RadioButton,
  } from "carbon-components-svelte";    
  export let question;
  export let questionnum;
  questionnum +=1;
  let questionstring = "Q."+ questionnum +"   ";
</script>


<Form>
    <FormGroup legendText={questionstring}{question.q}>
        <RadioButtonGroup name={question.id} orientation="vertical">
            {#each question.opt as option (option.id)}
                <RadioButton labelText={option.a} value={option.a}></RadioButton>
	        {/each}
        </RadioButtonGroup>
    </FormGroup>
</Form>