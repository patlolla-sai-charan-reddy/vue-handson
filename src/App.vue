<template>
  <hot-table :settings="settings" id="app"></hot-table>
</template>

<script>
import { HotTable } from "@handsontable-pro/vue";

let x = [
  [
    1,
    3,
    1,
    112,
    13,
    12,
    15,
    14,
    16,
    17,
    18,
    19,
    20,
    21,
    2,
    4,
    5,
    6,
    7,
    8,
    9,
    0,
    22,
    23,
    24,
    25,
    26
  ],
  [
    1,
    4,
    1,
    11,
    13,
    12,
    15,
    14,
    16,
    17,
    18,
    19,
    20,
    21,
    2,
    4,
    5,
    6,
    7,
    8,
    9,
    0,
    22,
    23,
    24,
    25,
    26
  ]
];

export default {
  data: function() {
    return {
      settings: {
        data: x,
        colHeaders: true,
        nestedHeaders: [
          [
            { label: "SFWC", colspan: 1 },
            { label: "MARKET PLACEMENT", colspan: 3 },
            { label: "TIMING", colspan: 1 },
            { label: "TRANSACTION TYPE", colspan: 3 },
            { label: "ISSUANCE", colspan: 7 },
            { label: "PARTIES TO THE TRANSACTION", colspan: 1 },
            { label: "RATING AGENCIES", colspan: 6 }
          ],
          [
            "DEAL ID",
            "REGION",
            "COUNTRY",
            "$",
            "PRICING DATE",
            "MANAGEMENT LINE",
            "SUBSECTOR (BROAD)",
            "MARKET SECTOR",
            "NAME",
            "CLASS NAME",
            "DEAL NAME",
            "AMOUNT (MM)",
            "ORIGINATOR",
            "ASSET MANAGER",
            "ARRANGER",
            "SPONSOR OF SPV",
            "FITCH",
            "S&P",
            "MOODY",
            "DBRS",
            "KROLL",
            "MORNING STAR",
            "PLACEMENT TYPE",
            "JURISDICTION",
            "REASONS NOT RATED",
            "REASONS NOT RATED COMMENTS",
            "IMPORT NOTES"
          ]
        ],
        rowHeaders: false,
        colWidths: 100,
        height: 200,
        className: "my-custom-classname"
      }
    };
  },
  components: {
    HotTable
  }
};
</script>

<style
  src="../node_modules/handsontable-pro/dist/handsontable.full.css"
></style>

<style>
#app {
  max-width: 800px;
}
</style>
