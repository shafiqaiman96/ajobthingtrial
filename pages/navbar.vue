<template>
	<b-navbar type="dark" variant="dark" style="padding-left: 200px;">
		<b-navbar-nav>
			<div class="pull-center pull-sm-reset text-center hidden-xs" style="float: left; padding-right: 10px; ">
				<a href="#">
					<img alt="Maukerja - Kerja Kosong &amp; Jawatan Kosong Terkini Malaysia" src="https://files.ajobthing.com/brightan-assets/images/maukerja/others/v1/top-logo-lg.png?version=1" height="38px">
				</a>
			</div>

			<b-nav-item active href="#">All jobs</b-nav-item>

			<!-- Navbar dropdowns -->
			<b-nav-item-dropdown text="User" left>
				<b-dropdown-item href="#">Top Companies</b-dropdown-item>
				<b-dropdown-item href="#">Resume Builder</b-dropdown-item>
			</b-nav-item-dropdown>

			<b-nav-item-dropdown text="Tools" left>
				<b-dropdown-item href="#">F.A.Q</b-dropdown-item>
				<b-dropdown-item href="#">Contact</b-dropdown-item>
				<b-dropdown-item href="#">About</b-dropdown-item>
			</b-nav-item-dropdown>

			<b-nav-item href="#">Blog</b-nav-item>
		</b-navbar-nav>
	</b-navbar>
</template>

<style scoped>

.navbar.navbar-dark.bg-dark{
    background-color: #db1435!important;
 }

.nav-link{
    color: #fff;
    background-color: #be2a43;
     }

.nav-link:not(.active){
    color: #fff;
    background-color: #db1435;
}



.form-control {
max-width:300px;
max-height: 30px;
border-bottom-left-radius:20px;
border-bottom-right-radius:20px;
border-top-left-radius:20px;
border-top-right-radius:20px}

</style>