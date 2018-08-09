<template>
    <div>
        <h1>Test</h1>
        <table class="table table-dark">
            <thead>
                <th>Name</th>
                <th>Email</th>
            </thead>
            <tbody>
                <td>{{contact.name}}</td>
                <td>{{contact.email}}</td>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    props: ['contact']
}
</script>
