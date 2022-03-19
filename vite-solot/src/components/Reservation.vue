<script setup lang="ts">
import { ref } from 'vue';
import Card from './Card.vue';
import Badge from './Badge.vue';
import ListReservation from './ListReservation.vue';
import ReservationList from './ReservationList.vue';

const isListVisible = ref<boolean>(true)

const isDialogOpen = ref<boolean>(false)

const onClickButton = () => {
    // isListVisible.value = !isListVisible.value
    isDialogOpen.value = !isDialogOpen.value
}

const getContent = () => {
    if (isListVisible.value) {
        return ReservationList;
    } else {
        return ListReservation;
    }
}
</script>

<template>
    <div class="container">
        <div class="card">
            <Card class="menu-card">
                <span>Badges</span>
                <div class="badges">
                    <Badge class="vip-badge">
                        <span>VIP</span>
                    </Badge>
                    <Badge class="normal-badge">
                        <span>Normal</span>
                    </Badge>
                </div>
            </Card>
        </div>
        <component :is="getContent()" />
        <!-- <div v-if="isListVisible">
            <ReservationList />
        </div>
        <div v-else>
            <ListReservation />
        </div> -->
        <button @click="onClickButton">change</button>
        <teleport to="body">
            <dialog class="dialog" :open="isDialogOpen">
                <span>Dialog</span>
            </dialog>
        </teleport>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.menu-card {
    width: 300px;
    height: 80px;
    background-color: #ccc;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 24px;
}

.badges {
    display: flex;
    justify-content: space-between;
    width: 60%;
}

.normal-badge {
    background-color: blue;
    color: white;
}

.vip-badge {
    background-color: #810036;
    color: white;
}

.dialog {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100px;
    width: 300px;
    margin: auto;
    background-color: aliceblue;
}
</style>