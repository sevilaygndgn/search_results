<template>
  <ul class="results-container">
    <li v-for="index in filteredProduct" :key="index" :index="index" class="items">
      <img src="../assets/images/1.png" alt="" />
      <div class="details">
        <span class="title">{{index.name}}</span>
        <span class="description">{{index.price.display.smart}}</span>
      </div>
    </li>
  </ul>
</template>
<script>
import { eventBus } from "@/main";
export default {
  data() {
    return {
      searchValue: '',
      items: [
        {
          type: "WUIP",
          name: "iPhone 13 Pro",
          baseName: "iPhone 13 Pro",
          id: "IPHONE13PRO_MAIN",
          price: {
            value: 999.0,
            display: {
              smart: "$999",
              actual: "$999.00",
              from: "From $999",
              monthlyFrom: "From $41.62/mo. for 24 mo. or $999",
              monthlyPrice: "From $41.62 for 24 mo.",
              perMonth: "$41.62/mo.",
              perMonthSmart: "$41.62",
              perMonthActual: "$41.62",
              perMonthValue: "41.62",
              months: "24",
              apr: "0 %",
            },
          },
          tradeIn: {
            slug: "model_iphone_11_pro",
            productName: "iPhone 11 Pro",
            maxPriceProductName: "iPhone 11 Pro",
            credit: {
              value: 300,
              display: {
                smart: "$300",
                upto: "Up to $300",
                actual: "$300.00",
                range: "$300-$300",
                minValue: "$300",
                maxValue: "$300",
              },
            },
            priceWithCreditApplied: {
              value: 699.0,
              display: {
                smart: "$699",
                actual: "$699.00",
                from: "From $699 with trade-in",
                monthlyFrom: "From $29.12/mo. for 24 mo. or $699 with trade-in",
                monthlyPrice: "From $29.12/mo. for 24 months with trade-in",
                perMonth: "$29.12/mo.",
                perMonthSmart: "$29.12",
                perMonthActual: "$29.12",
                perMonthValue: "29.12",
                months: "24",
                apr: "0 %",
              },
            },
            legal:
              "Trade-in values will vary based on the condition, year, and configuration of your eligible trade-in device. Not all devices are eligible for credit. You must be at least 18 years old to be eligible to trade in for credit or for an Apple Gift Card. Trade-in value may be applied toward qualifying new device purchase, or added to an Apple Gift Card. Actual value awarded is based on receipt of a qualifying device matching the description provided when estimate was made. Sales tax may be assessed on full value of a new device purchase. In-store trade-in requires presentation of a valid photo ID (local law may require saving this information). Offer may not be available in all stores, and may vary between in-store and online trade-in. Some stores may have additional requirements. Apple or its trade-in partners reserve the right to refuse or limit quantity of any trade-in transaction for any reason. More details are available from Apple’s trade-in partner for trade-in and recycling of eligible devices. Restrictions and limitations may apply.",
          },
        },
        {
          type: "WUIP",
          name: "iPhone 12",
          baseName: "iPhone 12",
          id: "IPHONE12_MAIN",
          price: {
            value: 599.0,
            display: {
              smart: "$599",
              actual: "$599.00",
              from: "From $599",
              monthlyFrom: "From $24.95/mo. for 24 mo. or $599",
              monthlyPrice: "From $24.95 for 24 mo.",
              perMonth: "$24.95/mo.",
              perMonthSmart: "$24.95",
              perMonthActual: "$24.95",
              perMonthValue: "24.95",
              months: "24",
              apr: "0 %",
            },
          },
          tradeIn: {
            slug: "model_iphone_xr",
            productName: "iPhone XR",
            maxPriceProductName: "iPhone XR",
            credit: {
              value: 160,
              display: {
                smart: "$160",
                upto: "Up to $160",
                actual: "$160.00",
                range: "$160-$160",
                minValue: "$160",
                maxValue: "$160",
              },
            },
            priceWithCreditApplied: {
              value: 439.0,
              display: {
                smart: "$439",
                actual: "$439.00",
                from: "From $439 with trade-in",
                monthlyFrom: "From $18.29/mo. for 24 mo. or $439 with trade-in",
                monthlyPrice: "From $18.29/mo. for 24 months with trade-in",
                perMonth: "$18.29/mo.",
                perMonthSmart: "$18.29",
                perMonthActual: "$18.29",
                perMonthValue: "18.29",
                months: "24",
                apr: "0 %",
              },
            },
            legal:
              "Trade-in values will vary based on the condition, year, and configuration of your eligible trade-in device. Not all devices are eligible for credit. You must be at least 18 years old to be eligible to trade in for credit or for an Apple Gift Card. Trade-in value may be applied toward qualifying new device purchase, or added to an Apple Gift Card. Actual value awarded is based on receipt of a qualifying device matching the description provided when estimate was made. Sales tax may be assessed on full value of a new device purchase. In-store trade-in requires presentation of a valid photo ID (local law may require saving this information). Offer may not be available in all stores, and may vary between in-store and online trade-in. Some stores may have additional requirements. Apple or its trade-in partners reserve the right to refuse or limit quantity of any trade-in transaction for any reason. More details are available from Apple’s trade-in partner for trade-in and recycling of eligible devices. Restrictions and limitations may apply.",
          },
        },
        {
          type: "WUIP",
          name: "iPhone SE",
          baseName: "iPhone SE",
          id: "IPHONESE3_MAIN",
          price: {
            value: 429.0,
            display: {
              smart: "$429",
              actual: "$429.00",
              from: "From $429",
              monthlyFrom: "From $17.87/mo. for 24 mo. or $429",
              monthlyPrice: "From $17.87 for 24 mo.",
              perMonth: "$17.87/mo.",
              perMonthSmart: "$17.87",
              perMonthActual: "$17.87",
              perMonthValue: "17.87",
              months: "24",
              apr: "0 %",
            },
          },
          tradeIn: {
            slug: "model_iphone_8",
            productName: "iPhone 8",
            maxPriceProductName: "iPhone 8",
            credit: {
              value: 90,
              display: {
                smart: "$90",
                upto: "Up to $90",
                actual: "$90.00",
                range: "$90-$90",
                minValue: "$90",
                maxValue: "$90",
              },
            },
            priceWithCreditApplied: {
              value: 339.0,
              display: {
                smart: "$339",
                actual: "$339.00",
                from: "From $339 with trade-in",
                monthlyFrom: "From $14.12/mo. for 24 mo. or $339 with trade-in",
                monthlyPrice: "From $14.12/mo. for 24 months with trade-in",
                perMonth: "$14.12/mo.",
                perMonthSmart: "$14.12",
                perMonthActual: "$14.12",
                perMonthValue: "14.12",
                months: "24",
                apr: "0 %",
              },
            },
            legal:
              "Trade-in values will vary based on the condition, year, and configuration of your eligible trade-in device. Not all devices are eligible for credit. You must be at least 18 years old to be eligible to trade in for credit or for an Apple Gift Card. Trade-in value may be applied toward qualifying new device purchase, or added to an Apple Gift Card. Actual value awarded is based on receipt of a qualifying device matching the description provided when estimate was made. Sales tax may be assessed on full value of a new device purchase. In-store trade-in requires presentation of a valid photo ID (local law may require saving this information). Offer may not be available in all stores, and may vary between in-store and online trade-in. Some stores may have additional requirements. Apple or its trade-in partners reserve the right to refuse or limit quantity of any trade-in transaction for any reason. More details are available from Apple’s trade-in partner for trade-in and recycling of eligible devices. Restrictions and limitations may apply.",
          },
        },
        {
          type: "WUIP",
          name: "iPhone 13",
          baseName: "iPhone 13",
          id: "IPHONE13_MAIN",
          price: {
            value: 699.0,
            display: {
              smart: "$699",
              actual: "$699.00",
              from: "From $699",
              monthlyFrom: "From $29.12/mo. for 24 mo. or $699",
              monthlyPrice: "From $29.12 for 24 mo.",
              perMonth: "$29.12/mo.",
              perMonthSmart: "$29.12",
              perMonthActual: "$29.12",
              perMonthValue: "29.12",
              months: "24",
              apr: "0 %",
            },
          },
          tradeIn: {
            slug: "model_iphone_11",
            productName: "iPhone 11",
            maxPriceProductName: "iPhone 11",
            credit: {
              value: 230,
              display: {
                smart: "$230",
                upto: "Up to $230",
                actual: "$230.00",
                range: "$230-$230",
                minValue: "$230",
                maxValue: "$230",
              },
            },
            priceWithCreditApplied: {
              value: 469.0,
              display: {
                smart: "$469",
                actual: "$469.00",
                from: "From $469 with trade-in",
                monthlyFrom: "From $19.54/mo. for 24 mo. or $469 with trade-in",
                monthlyPrice: "From $19.54/mo. for 24 months with trade-in",
                perMonth: "$19.54/mo.",
                perMonthSmart: "$19.54",
                perMonthActual: "$19.54",
                perMonthValue: "19.54",
                months: "24",
                apr: "0 %",
              },
            },
            legal:
              "Trade-in values will vary based on the condition, year, and configuration of your eligible trade-in device. Not all devices are eligible for credit. You must be at least 18 years old to be eligible to trade in for credit or for an Apple Gift Card. Trade-in value may be applied toward qualifying new device purchase, or added to an Apple Gift Card. Actual value awarded is based on receipt of a qualifying device matching the description provided when estimate was made. Sales tax may be assessed on full value of a new device purchase. In-store trade-in requires presentation of a valid photo ID (local law may require saving this information). Offer may not be available in all stores, and may vary between in-store and online trade-in. Some stores may have additional requirements. Apple or its trade-in partners reserve the right to refuse or limit quantity of any trade-in transaction for any reason. More details are available from Apple’s trade-in partner for trade-in and recycling of eligible devices. Restrictions and limitations may apply.",
          },
        },
      ],
    };
  },
    computed: {
    filteredProduct() {
      return this.items.filter((item) => {
        return item.name
          .toLocaleLowerCase()
          .includes(this.searchValue.toLocaleLowerCase());
      });
    },
  },
  created() {
    eventBus.$on("searchProduct", (data) => {
        this.searchValue = data;
    });
  },
};
</script>
<style lang="scss" scoped>
.results-container {
  display: grid;
  background-color: #fff;
  width: 300px;
  padding: 13px;
  .items {
    background-color: #fff;
    display: flex;
    align-items: center;
    padding: 20px;
    height: 100px;
    img {
      margin-right: 15px;
      width: 60px;
      height: 60px;
    }
    .details {
      display: grid;
      .title {
        font-weight: bold;
        font-size: 16px;
        line-height: 24px;
        color: #2c3e50;
      }
      .description {
        font-weight: 400;
        font-size: 12px;
        line-height: 21px;
        color: #2c3e50;
      }
    }
  }
}
</style>
