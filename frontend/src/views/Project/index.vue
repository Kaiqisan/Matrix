<template>
	<div>
		<el-container style="margin: 20px 70px">
			<el-main>
				<el-row>
					<el-col
						:span="screenWidth > 1400 ? 6 : screenWidth <= 1400 && screenWidth >= 900 ? 8 : screenWidth <= 900 && screenWidth >= 500 ? 12 : 24"
						v-for="(o, index) in 10"
						:key="o">
						<el-card
							:body-style="{ padding: '0px' }"
							style="margin: 20px">
							<img
								src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"
								class="image" alt="">
							<div style="padding: 14px;">
								<span>好吃的汉堡</span>
								<div class="bottom clearfix">
									<time class="time">Alex</time>
									<el-button type="text" class="button">操作按钮</el-button>
								</div>
							</div>
						</el-card>
					</el-col>
				</el-row>
			</el-main>
		</el-container>
	</div>
</template>

<script>
    export default {
        name: 'Project',
		props: ['screenWidth'],
        data() {
            return {
                projectList: [
                    {
                        title: 'AI New Knowledge 机器学习可视化平台',
                        url: 'http://39.107.250.76/flow/',
                        repositories: 'https://github.com/Matrix-King-Studio/MachineLearningAlgorithmPlatform',
                    }
                ],
				width: 1500
            }
        },
        watch: {
            screenWidth: {
                handler(val) {
					// console.log(val);
                },
                immediate: true
            }
        },
    }
</script>

<style scoped>
	.time {
		font-size: 13px;
		color: #999;
	}

	.bottom {
		margin-top: 13px;
		line-height: 12px;
	}

	.button {
		padding: 0;
		float: right;
	}

	.image {
		width: 100%;
		display: block;
	}

	.clearfix:before,
	.clearfix:after {
		display: table;
		content: "";
	}

	.clearfix:after {
		clear: both
	}
</style>