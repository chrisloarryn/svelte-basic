<script>
    let value = ''
    let response = []
    const handleInput = (event) => 
        value = event.target.value
    
    $: if (value !== '' && value.length >= 5) {
        const findUrl = `http://www.omdbapi.com/?s=${value}&apiKey=26d2542c`
        fetch(findUrl).then(res => res.json()).then(apiResponse => {
            response = apiResponse.Search
        })
    }
</script>

<input value={value} on:input={handleInput} />