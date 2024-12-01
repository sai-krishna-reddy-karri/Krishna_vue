<template>
    <div>
        <h1>
            <i class="fa fa-store"></i> <!-- Store icon from Font Awesome -->
            {{ heading }}
        </h1>
    </div>
</template>

<script>
export default {
    name: 'DeliHeader',
    props: {
        heading: String
    }
};
</script>

<style scoped>
/* Center-align text, make it italic, and add padding */
* {
    text-align: center;
    padding: 10px;
}

h1 {
    font-style: italic;
    display: flex; /* Use flexbox to align the icon and text */
    align-items: center; /* Align items vertically */
    justify-content: center; /* Center the content */
    gap: 10px; /* Space between the icon and text */
}

h1 i {
    font-size: 24px; /* Adjust the icon size */
}
</style>
