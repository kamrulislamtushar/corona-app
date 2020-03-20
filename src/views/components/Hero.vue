<template>
    <div class="profile-page">
        <section class="section-profile-cover section-shaped my-0">
            <div class="shape shape-style-1 shape-primary shape-skew alpha-4">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
            </div>
        </section>
        <section class="section section-skew">
            <div class="container align-items-center">
                <card shadow class="card-profile h-80vh mt--300" no-body>
                    <div class="px-4 text-center mt-auto mb-auto ">
                        <form-wizard  title="অনলাইনে করোনা ভাইরাস ঝুঁকি পরীক্ষা" subtitle=""
                                     back-button-text="পূর্ববর্তী"
                                     next-button-text="পরবর্তী"
                                     finish-button-text="সম্পন্ন"
                                     color="#5e72e4"
                        >
                            <tab-content icon="fa fa-user" title="বয়স">
                                <h3 class="mt-5 mb-5">বাটনটি দিয়ে আপনার বয়স নির্ধারণ করুন</h3>
                                <base-slider :range="{min: 2, max: 100}" v-model="slider"></base-slider>
                                <h3> {{ slider }} বছর </h3>
                            </tab-content>

                            <tab-content title="জ্বর" icon="ti ti-dashboard">
                                <div class="row">
                                    <div class="col mb-5">
                                        <h3 class="mb-4">আপনার কি জ্বর আছে ?</h3>
                                        <h5>অর্থাৎ, শরীরের তাপমাত্রা ৩৭.৫°C অথবা, ৯৮.৪°F থেকে বেশি ?</h5>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="শ্বাসকষ্ট" icon="ti ti-pulse">
                                <div class="row mb-5">
                                    <div class="col ">
                                        <h3 class="mb-4">আপনার কি শ্বাসকষ্ট আছে বা শ্বাস নিতে বা ফেলতে কোন কষ্ট হচ্ছে ?</h3>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="শারীরিক দূর্বলতা" icon="ti ti-info-alt">
                                <div class="row mb-5">
                                    <div class="col">
                                        <h3 class="mb-4">আপনার কি কাশি এবং শারীরিক দূর্বলতা আছে ?</h3>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="সর্দি, গলাব্যথা" icon="ti ti-thought">
                                <div class="row mb-5">
                                    <div class="col">
                                        <h3 class="mb-4">আপনার, সর্দি, গলাব্যথা আছে বা ঢোক গিলতে সমস্যা হয় ?</h3>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="বিদেশ ভ্রমণ" icon="ti ti-location-arrow">
                                <div class="row mb-5">
                                    <div class="col">
                                        <h3 class="mb-4">আপনি কি গত ১৪ দিনের ভিতরে কোভিড- ১৯ ( করোনা) এ আক্রান্ত কোন দেশ চীন, ইতালি, দক্ষিণ কোরিয়া, জাপান, সিংগাপুর, আমেরিকা, বা ইউরোপের দেশে ভ্রমণ করেছেন ?</h3>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="আক্রান্ত ব্যক্তির সংস্পর্শ" icon="ti ti-hand-drag">
                                <div class="row mb-5">
                                    <div class="col">
                                        <h3 class="mb-4">আপনি কি কোভিড- ১৯ ( করোনা) এ আক্রান্ত কোন ব্যক্তির সংস্পর্শে ছিলেন ( একই সাথে অবস্থান, বা ভ্রমন করেছেন) ?</h3>
                                    </div>
                                </div>
                                <div class="row mb-2 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block  type="primary">হ্যা</base-button>
                                    </div>
                                </div>
                                <div class="row mb-5 text-center">
                                    <div class="col text-align-webkit-center">
                                        <base-button block type="primary">না</base-button>
                                    </div>
                                </div>
                            </tab-content>
                            <tab-content title="" icon="ti ti-check">
                                We are Almost Finished
                            </tab-content>
                        </form-wizard>
                    </div>
                </card>
            </div>
        </section>
    </div>
</template>
<script>
export default {
  data() {
    return {
      slider: 35,
    }
  }
};
</script>
<style>
</style>
