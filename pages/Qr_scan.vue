<template>
    <div>
        <h2>QR scanner</h2>
        <QrScan />
    </div>
</template>
<script>
import Qr_Scan from '~/components/Qr_Scan.vue'

export default{
    components: { Qr_Scan}
}
</script>