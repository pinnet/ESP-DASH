<template>
<nav class="navbar">
  <div class="navbar-brand">
    <a class="navbar-item" href="/">
      <img src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcKICAgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIgogICB4bWxuczpjYz0iaHR0cDovL2NyZWF0aXZlY29tbW9ucy5vcmcvbnMjIgogICB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiCiAgIHhtbG5zOnN2Zz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM6c29kaXBvZGk9Imh0dHA6Ly9zb2RpcG9kaS5zb3VyY2Vmb3JnZS5uZXQvRFREL3NvZGlwb2RpLTAuZHRkIgogICB4bWxuczppbmtzY2FwZT0iaHR0cDovL3d3dy5pbmtzY2FwZS5vcmcvbmFtZXNwYWNlcy9pbmtzY2FwZSIKICAgdmlld0JveD0iMCAtMjU2IDE5NTAgMTk1MCIKICAgaWQ9InN2ZzMwMDEiCiAgIHZlcnNpb249IjEuMSIKICAgaW5rc2NhcGU6dmVyc2lvbj0iMC40OC4zLjEgcjk4ODYiCiAgIHdpZHRoPSIxMDAlIgogICBoZWlnaHQ9IjEwMCUiCiAgIHNvZGlwb2RpOmRvY25hbWU9ImZvbGRlcl9vcGVuX2FsdF9mb250X2F3ZXNvbWUuc3ZnIj4KICA8bWV0YWRhdGEKICAgICBpZD0ibWV0YWRhdGEzMDExIj4KICAgIDxyZGY6UkRGPgogICAgICA8Y2M6V29yawogICAgICAgICByZGY6YWJvdXQ9IiI+CiAgICAgICAgPGRjOmZvcm1hdD5pbWFnZS9zdmcreG1sPC9kYzpmb3JtYXQ+CiAgICAgICAgPGRjOnR5cGUKICAgICAgICAgICByZGY6cmVzb3VyY2U9Imh0dHA6Ly9wdXJsLm9yZy9kYy9kY21pdHlwZS9TdGlsbEltYWdlIiAvPgogICAgICA8L2NjOldvcms+CiAgICA8L3JkZjpSREY+CiAgPC9tZXRhZGF0YT4KICA8ZGVmcwogICAgIGlkPSJkZWZzMzAwOSIgLz4KICA8c29kaXBvZGk6bmFtZWR2aWV3CiAgICAgcGFnZWNvbG9yPSIjZmZmZmZmIgogICAgIGJvcmRlcmNvbG9yPSIjNjY2NjY2IgogICAgIGJvcmRlcm9wYWNpdHk9IjEiCiAgICAgb2JqZWN0dG9sZXJhbmNlPSIxMCIKICAgICBncmlkdG9sZXJhbmNlPSIxMCIKICAgICBndWlkZXRvbGVyYW5jZT0iMTAiCiAgICAgaW5rc2NhcGU6cGFnZW9wYWNpdHk9IjAiCiAgICAgaW5rc2NhcGU6cGFnZXNoYWRvdz0iMiIKICAgICBpbmtzY2FwZTp3aW5kb3ctd2lkdGg9IjY0MCIKICAgICBpbmtzY2FwZTp3aW5kb3ctaGVpZ2h0PSI0ODAiCiAgICAgaWQ9Im5hbWVkdmlldzMwMDciCiAgICAgc2hvd2dyaWQ9ImZhbHNlIgogICAgIGlua3NjYXBlOnpvb209IjAuMTMxNjk2NDMiCiAgICAgaW5rc2NhcGU6Y3g9Ijk1NC41IgogICAgIGlua3NjYXBlOmN5PSI4OTYiCiAgICAgaW5rc2NhcGU6d2luZG93LXg9IjAiCiAgICAgaW5rc2NhcGU6d2luZG93LXk9IjI1IgogICAgIGlua3NjYXBlOndpbmRvdy1tYXhpbWl6ZWQ9IjAiCiAgICAgaW5rc2NhcGU6Y3VycmVudC1sYXllcj0ic3ZnMzAwMSIgLz4KICA8ZwogICAgIHRyYW5zZm9ybT0ibWF0cml4KDEsMCwwLC0xLDMwLjM3Mjg4MSwxNDQzLjQyMzcpIgogICAgIGlkPSJnMzAwMyI+CiAgICA8cGF0aAogICAgICAgZD0ibSAxNzgxLDYwNSBxIDAsMzUgLTUzLDM1IEggNjQwIFEgNjAwLDY0MCA1NTQuNSw2MTguNSA1MDksNTk3IDQ4Myw1NjYgTCAxODksMjAzIHEgLTE4LC0yNCAtMTgsLTQwIDAsLTM1IDUzLC0zNSBoIDEwODggcSA0MCwwIDg2LDIyIDQ2LDIyIDcxLDUzIGwgMjk0LDM2MyBxIDE4LDIyIDE4LDM5IHogTSA2NDAsNzY4IGggNzY4IHYgMTYwIHEgMCw0MCAtMjgsNjggLTI4LDI4IC02OCwyOCBIIDczNiBxIC00MCwwIC02OCwyOCAtMjgsMjggLTI4LDY4IHYgNjQgcSAwLDQwIC0yOCw2OCAtMjgsMjggLTY4LDI4IEggMjI0IHEgLTQwLDAgLTY4LC0yOCAtMjgsLTI4IC0yOCwtNjggViAzMzEgbCAyNTYsMzE1IHEgNDQsNTMgMTE2LDg3LjUgNzIsMzQuNSAxNDAsMzQuNSB6IE0gMTkwOSw2MDUgcSAwLC02MiAtNDYsLTEyMCBMIDE1NjgsMTIyIFEgMTUyNSw2OSAxNDUyLDM0LjUgMTM3OSwwIDEzMTIsMCBIIDIyNCBRIDEzMiwwIDY2LDY2IDAsMTMyIDAsMjI0IHYgOTYwIHEgMCw5MiA2NiwxNTggNjYsNjYgMTU4LDY2IGggMzIwIHEgOTIsMCAxNTgsLTY2IDY2LC02NiA2NiwtMTU4IHYgLTMyIGggNTQ0IHEgOTIsMCAxNTgsLTY2IDY2LC02NiA2NiwtMTU4IFYgNzY4IGggMTkyIHEgNTQsMCA5OSwtMjQuNSA0NSwtMjQuNSA2NywtNzAuNSAxNSwtMzIgMTUsLTY4IHoiCiAgICAgICBpZD0icGF0aDMwMDUiCiAgICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgICAgc3R5bGU9ImZpbGw6Y3VycmVudENvbG9yIiAvPgogIDwvZz4KPC9zdmc+Cg==" alt="DASH [Connected]"  width="100px" :class="{'is-hidden': !connected}">
      <img src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcKICAgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIgogICB4bWxuczpjYz0iaHR0cDovL2NyZWF0aXZlY29tbW9ucy5vcmcvbnMjIgogICB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiCiAgIHhtbG5zOnN2Zz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM6c29kaXBvZGk9Imh0dHA6Ly9zb2RpcG9kaS5zb3VyY2Vmb3JnZS5uZXQvRFREL3NvZGlwb2RpLTAuZHRkIgogICB4bWxuczppbmtzY2FwZT0iaHR0cDovL3d3dy5pbmtzY2FwZS5vcmcvbmFtZXNwYWNlcy9pbmtzY2FwZSIKICAgdmlld0JveD0iMCAtMjU2IDE5NTAgMTk1MCIKICAgaWQ9InN2ZzMwMDEiCiAgIHZlcnNpb249IjEuMSIKICAgaW5rc2NhcGU6dmVyc2lvbj0iMC40OC4zLjEgcjk4ODYiCiAgIHdpZHRoPSIxMDAlIgogICBoZWlnaHQ9IjEwMCUiCiAgIHNvZGlwb2RpOmRvY25hbWU9ImZvbGRlcl9vcGVuX2FsdF9mb250X2F3ZXNvbWUuc3ZnIj4KICA8bWV0YWRhdGEKICAgICBpZD0ibWV0YWRhdGEzMDExIj4KICAgIDxyZGY6UkRGPgogICAgICA8Y2M6V29yawogICAgICAgICByZGY6YWJvdXQ9IiI+CiAgICAgICAgPGRjOmZvcm1hdD5pbWFnZS9zdmcreG1sPC9kYzpmb3JtYXQ+CiAgICAgICAgPGRjOnR5cGUKICAgICAgICAgICByZGY6cmVzb3VyY2U9Imh0dHA6Ly9wdXJsLm9yZy9kYy9kY21pdHlwZS9TdGlsbEltYWdlIiAvPgogICAgICA8L2NjOldvcms+CiAgICA8L3JkZjpSREY+CiAgPC9tZXRhZGF0YT4KICA8ZGVmcwogICAgIGlkPSJkZWZzMzAwOSIgLz4KICA8c29kaXBvZGk6bmFtZWR2aWV3CiAgICAgcGFnZWNvbG9yPSIjZmZmZmZmIgogICAgIGJvcmRlcmNvbG9yPSIjNjY2NjY2IgogICAgIGJvcmRlcm9wYWNpdHk9IjEiCiAgICAgb2JqZWN0dG9sZXJhbmNlPSIxMCIKICAgICBncmlkdG9sZXJhbmNlPSIxMCIKICAgICBndWlkZXRvbGVyYW5jZT0iMTAiCiAgICAgaW5rc2NhcGU6cGFnZW9wYWNpdHk9IjAiCiAgICAgaW5rc2NhcGU6cGFnZXNoYWRvdz0iMiIKICAgICBpbmtzY2FwZTp3aW5kb3ctd2lkdGg9IjY0MCIKICAgICBpbmtzY2FwZTp3aW5kb3ctaGVpZ2h0PSI0ODAiCiAgICAgaWQ9Im5hbWVkdmlldzMwMDciCiAgICAgc2hvd2dyaWQ9ImZhbHNlIgogICAgIGlua3NjYXBlOnpvb209IjAuMTMxNjk2NDMiCiAgICAgaW5rc2NhcGU6Y3g9Ijk1NC41IgogICAgIGlua3NjYXBlOmN5PSI4OTYiCiAgICAgaW5rc2NhcGU6d2luZG93LXg9IjAiCiAgICAgaW5rc2NhcGU6d2luZG93LXk9IjI1IgogICAgIGlua3NjYXBlOndpbmRvdy1tYXhpbWl6ZWQ9IjAiCiAgICAgaW5rc2NhcGU6Y3VycmVudC1sYXllcj0ic3ZnMzAwMSIgLz4KICA8ZwogICAgIHRyYW5zZm9ybT0ibWF0cml4KDEsMCwwLC0xLDMwLjM3Mjg4MSwxNDQzLjQyMzcpIgogICAgIGlkPSJnMzAwMyI+CiAgICA8cGF0aAogICAgICAgZD0ibSAxNzgxLDYwNSBxIDAsMzUgLTUzLDM1IEggNjQwIFEgNjAwLDY0MCA1NTQuNSw2MTguNSA1MDksNTk3IDQ4Myw1NjYgTCAxODksMjAzIHEgLTE4LC0yNCAtMTgsLTQwIDAsLTM1IDUzLC0zNSBoIDEwODggcSA0MCwwIDg2LDIyIDQ2LDIyIDcxLDUzIGwgMjk0LDM2MyBxIDE4LDIyIDE4LDM5IHogTSA2NDAsNzY4IGggNzY4IHYgMTYwIHEgMCw0MCAtMjgsNjggLTI4LDI4IC02OCwyOCBIIDczNiBxIC00MCwwIC02OCwyOCAtMjgsMjggLTI4LDY4IHYgNjQgcSAwLDQwIC0yOCw2OCAtMjgsMjggLTY4LDI4IEggMjI0IHEgLTQwLDAgLTY4LC0yOCAtMjgsLTI4IC0yOCwtNjggViAzMzEgbCAyNTYsMzE1IHEgNDQsNTMgMTE2LDg3LjUgNzIsMzQuNSAxNDAsMzQuNSB6IE0gMTkwOSw2MDUgcSAwLC02MiAtNDYsLTEyMCBMIDE1NjgsMTIyIFEgMTUyNSw2OSAxNDUyLDM0LjUgMTM3OSwwIDEzMTIsMCBIIDIyNCBRIDEzMiwwIDY2LDY2IDAsMTMyIDAsMjI0IHYgOTYwIHEgMCw5MiA2NiwxNTggNjYsNjYgMTU4LDY2IGggMzIwIHEgOTIsMCAxNTgsLTY2IDY2LC02NiA2NiwtMTU4IHYgLTMyIGggNTQ0IHEgOTIsMCAxNTgsLTY2IDY2LC02NiA2NiwtMTU4IFYgNzY4IGggMTkyIHEgNTQsMCA5OSwtMjQuNSA0NSwtMjQuNSA2NywtNzAuNSAxNSwtMzIgMTUsLTY4IHoiCiAgICAgICBpZD0icGF0aDMwMDUiCiAgICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgICAgc3R5bGU9ImZpbGw6Y3VycmVudENvbG9yIiAvPgogIDwvZz4KPC9zdmc+Cg==" alt="Dash [Disconnected]" width="100px" :class="{'is-hidden': connected}">
    </a><span class="heading">Card Name&nbsp;</span>
    <span class="device-use">1.2Gb/8Gb   6.8Gb Free</span>
    <div class="navbar-burger burger" @click="toggleNavbar">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </div>

  <div class="navbar-menu" :class="{'is-active': open}">
    <div class="navbar-end">
      <router-link tag="a" class="navbar-item" to="/" exact>
        <div class="icon"><home-icon></home-icon></div> <span class="is-hidden-desktop"> &nbsp; Home</span>
      </router-link>
      <router-link tag="a" class="navbar-item" to="/stats" exact>
        <div class="icon"><zap-icon></zap-icon></div> <span class="is-hidden-desktop"> &nbsp; Stats</span>
      </router-link>
      <router-link tag="a" class="navbar-item" to="/about" exact>
        <div class="icon"><info-icon></info-icon></div> <span class="is-hidden-desktop"> &nbsp; About</span>
      </router-link>
    </div>
  </div>
</nav>
</template>

<script>
import { ZapIcon, HomeIcon, InfoIcon } from 'vue-feather-icons'

export default {
    props:['connected'],

    components: {
        ZapIcon,
        HomeIcon,
        InfoIcon
    },

    data(){
      return{
        open: false
      }
    },

    methods:{
      toggleNavbar(){
        this.open = !this.open;
      }
    }
}
</script>

<style>
.device-use{
  padding-top:42px;
  font-size:small;
}
.heading{
  padding-top:20px;
  font-size: xx-large;
}

.navbar{
    min-height: 80px !important;
    box-shadow: 0px 0px 60px rgba(232,232,232, 0.8);
    padding-left: 1rem;
    padding-right: 2rem;
}

.navbar-menu{
  padding: 1.5rem 0;
  box-shadow: none !important;
}

.navbar-item{
  border-radius: 6px;
  margin-left: 0.8rem;
}

@media screen and (max-width: 768px) {
    .navbar{
        padding-right: 1rem !important;
    }

    .navbar-brand{
        padding-top: 10px;
    }
}

@media screen and (min-width: 768px) {

  .navbar-item.is-active span{
    display: block !important;
  }
}

.navbar-item img{
    min-height: 2.75rem !important;
}

.navbar-item.is-active{
  background-color: #fafafa !important;
  color: #3273dc !important;
}

.button{
    padding-left: 20px !important;
    padding-right: 20px !important;
}

.icon{
    width: 16px !important;
    height: 16px !important;
    vertical-align: middle;
}
</style>
