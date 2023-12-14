<script>
import { store } from "../store.js" //state management

export default {
    name: "AppFooter",
    data() {
        return {
            store
        }
    },
    methods: {
        doThings() {
            console.log("AppComponent does things");
        }
    },
    mounted() {

    }
}
</script>

<template>
    <footer>
        <div>
            <ol>
                <h3>BOOKINGS</h3>
                <li>502 New Design Str,</li>
                <li>Melbourne, San Francisco,</li>
                <li>CA 94110, United States Of</li>
                <li>America​ Australia</li>
                <li>T: 1 123-456-789</li>
                <li>Email:demo@example.com</li>
            </ol>
        </div>
        <div>
            <ol>
                <h3>INFORMATION</h3>
                <li>Product Support</li>
                <li>Checkout</li>
                <li>Report Abuse</li>
                <li>Redeem Voucher</li>
                <li>Order Status</li>
            </ol>
        </div>
        <div>
            <ol>
                <h3>SUPPORT</h3>
                <li>Policies & Rules</li>
                <li>Privacy Policy</li>
                <li>License Policy</li>
                <li>My Account</li>
                <li>Locality</li>
            </ol>
        </div>
        <div>
            <div>NEWSLETTER</div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
// importo variabili
// @use './styles/partials/variables' as *;
footer {
    background-color: black;
    height: 25rem;
    display: flex;
}

ol li {
    list-style-type: none;
    padding: 4%;
}

footer div {
    margin: 0 4%;
}

// ...qui eventuale SCSS di AppComponent
</style>
