<template>
    <div class="footer-options">
        <div class="main-container">
            <div class=" button history">
                <span class="material-symbols-outlined">history</span>
            </div>
            <div class="button saved">
                <span class="material-symbols-outlined">star</span>
            </div>
            <div class="button contribute">
                <span class="material-symbols-outlined">group</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'FooterOptions'
}
</script>

<style scoped>
.footer-options {
    margin: 0 auto;
    width: 1100px;
}

.main-container {
    margin: 0 auto;
    width: 360px;
    padding: 12px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.button {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #bbb;
    border-radius: 50%;
    padding: 16px;
}

.material-symbols-outlined {
  font-size: 36px;
  color: #777;
  font-variation-settings:
  'FILL' 1,
  'wght' 400,
  'GRAD' 0,
  'opsz' 48
}

</style>