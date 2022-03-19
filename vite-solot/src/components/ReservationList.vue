<script setup lang="ts">
import Card from './Card.vue';
import Badge from './Badge.vue';

</script>

<template>
    <div>
        <Card class="reservation-card">
            <span>John Wick</span>
            <span>Badges</span>
            <Badge class="vip-badge">
                <span >VIP</span>
            </Badge>
        </Card>
        <Card class="reservation-card">
            <span>ito</span>
            <span>Badges</span>
            <Badge class="normal-badge">
                <span>Normal</span>
            </Badge>            
        </Card>
        <Card class="reservation-card">
            <span>tanaka</span>
            <span>Badges</span>
            <Badge class="vip-badge">
                <span>VIP</span>
            </Badge>
        </Card>
    </div>
</template>

<style scoped>
.reservation-card {
    width: 400px;
    height: 60px;
    background-color: rgb(255, 212, 147);
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 8px;
}

.normal-badge {
    background-color: blue;
    color: white;
}

.vip-badge {
    background-color: #810036;
    color: white;
}

</style>