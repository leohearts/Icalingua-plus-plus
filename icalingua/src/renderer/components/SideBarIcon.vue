<template>
    <a @click="$emit('click')" @click.middle="$emit('click-middle')" @click.right="$emit('click-right')">
        <div :class="{ selected }">
            <i :class="icon"></i>
            <br />
            {{ name }}
        </div>
    </a>
</template>

<script>
export default {
    name: 'SideBarIcon',
    props: {
        icon: String,
        name: String,
        selected: Boolean,
    },
}
</script>

<style scoped>
.selected {
    color: #19bdd2;
}
a {
    cursor: pointer;
}
a > div {
    margin-top: 20px;
    font-size: 12px;
    word-break: break-all;
}
a > div > i {
    font-size: 24px;
}
</style>
