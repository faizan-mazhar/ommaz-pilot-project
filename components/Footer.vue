<template>
  <div class="footer-section">
    <div class="footer-container">
      <div class="footer-row">
        <div class="footer-links">
          <a href="">Imprint</a>
          <a href="">Data Security</a>
          <a href="">Conditions</a>
          <a href="">Cookies</a>
          <a href="">Customs Support</a>
        </div>
        <div class="copyright-details">
          © 2021 Customs Support Group. All rights reserved.
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.footer-section {
  display: flex;
  background-color: white;
  padding: 50px 0;
  .footer-container {
    max-width: 1270px;
    margin: auto;
    color: black;
    width: 100%;
    @media (max-width: 1440px) {
      width: 80%;
    }
    .footer-row {
      display: flex;
      justify-content: space-between;
      width: 100%;
      @media (max-width: 1024px) {
        flex-direction: column;
      }
      .footer-links {
        a {
          margin-right: 10px;
          font-size: 16px;
          font-weight: bold;
          @media (max-width: 1024px) {
            display: flex;
            padding: 10px 0;
            flex-direction: column;
            border-bottom: 1px solid #ccc;
          }
          &:hover {
            color: #01a4b7;
          }
        }
      }
      .copyright-details {
        font-weight: 400;
        @media (max-width: 1024px) {
          margin-top: 20px;
        }
      }
    }
  }
}
</style>
