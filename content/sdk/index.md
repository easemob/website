---
title: 环信即时通讯云
layout: overview1
---

<script type="text/javascript" src="/js/analyticsCount.js"></script>
<script>
var _hmt = _hmt || [];
</script>
<div class="wrap_bd">
	<div class="download_wrap">
		<div class="w990">
			<div class="step_info">
				<h2>SDK下载<span>环信即时通讯云SDK是永久免费的，只需要花费你几分钟的时间就可以部署到你的项目中去</span></h2>
				<p>
					1.在环信开发者后台注册并且创建应用，就可以获得环信即时通讯云SDK的Appkey<br />
					2.下载环信即时通讯云SDK<br />
					3.只需在您的APP中加入几行简单的代码即可拥有强大的即时通讯功能（IM），详情参考官方DEMO及集成帮助文档
				</p>
				<ul class="step_icon">
					<li>
						<span class="ios_icon"></span>
						<a class="ios_btn" id="iosHref" onclick="_hmt.push(['_trackEvent', 'IMSDK', 'click', 'iosSDK'])" href=" http://downloads.easemob.com/downloads/IOSSDK-20150813.zip">下载IOS版开发包（SDK+文档+Demo)</a>
 						
						<span><em><a href="/docs/ios/quickstart"  target="_blank">5分钟快速入门</a> | <a href="/docs/ios/singlechat" target="_blank">iOS SDK 集成指南</a></em>V 2.2.0　</span>
					</li>
					<li class="li_away">
						<span class="andriod_icon"></span>
						<a  id="androidHref" class="ios_btn andriod_btn" onclick="_hmt.push(['_trackEvent', 'IMSDK', 'click', 'AndroidSDK'])" href="http://www.easemob.com/downloads/easemob-sdk-2.2.2.zip">下载Andriod版开发包（SDK+文档+Demo)</a>
 						
						<span><em><a href="/docs/android/quickstart"  target="_blank">5分钟快速入门</a> | <a href="/docs/android/singlechat" target="_blank">Android SDK 集成指南</a></em>V 2.2.2　</span>
					</li>
					<li class="li_away li_web">
						<span class="webIm_icon"></span>
						<a  id="androidHref" class="ios_btn web_btn" onclick="_hmt.push(['_trackEvent', 'IMSDK', 'click', 'AndroidSDK'])" href="http://downloads.easemob.com/downloads/WEB-IM-20150311.zip">下载WebIM版开发包（SDK+文档+Demo)</a>
 						
						<span><em><a href="/docs/webim/quickstart"  target="_blank">5分钟快速入门</a> | <a href="/docs/webim/quickstartinapp/" target="_blank">WebIM SDK 集成指南</a></em>V 1.0.5　</span>
					</li>
				</ul>
			</div>
		</div>
		<div class="clearfix"></div>
		<div id="container">
			<div class="history_date">
				<ul class="history_left">
			      	<h2 class="first">iOS SDK 更新日志</h2>
			      		<li>
                            <h3><em></em><span>版本：V2.2.0 2015-08-13</span></h3>
                            <dl>
                                <dt>
                                    <span>新功能：<br/>
                                    1、Demo集成parse SDK，展示如何获取联系人头像和昵称。 <br/>
                                    </span>

                                    <span> bug fix:<br/>
                                    1、SDK bug: 修复当离线消息数为0时回调的bug。<br/>
                                    2、SDK bug: 当群组创建时群组实际人数错误bug。<br/>
                                    3、SDK bug: 图片发送时按照图片分辨率进行剪裁压缩,保证图片正常显示。<br/>
                                    </span>

                                    <span>SDK细节调整：<br/>
                                    1、SDK支持iOS9;<br/>
                                    2、图片发送支持按原分辨率发送图片<a href="http://www.easemob.com/docs/ios/releaseNote2_2_0">2.2.0release note</a>。<br/> <br/>
                                    </span>
                                </dt>
                            </dl>
                        </li>
			      		<li>
                            <h3><em></em><span>版本：V2.1.9 2015-07-10</span></h3>
                            <dl>
                                <dt>
                                    <span>新功能：<br/>
                                    1、环信小助手功能，可自动回复，在demo中有体现。 <br/>
                                    </span>

                                    <span> bug fix:<br/>
                                    1、demo bug: 好友删除, 对应的会话不被删除。<br/>
                                    </span>

                                    <span>SDK细节调整：<br/>
                                    1、使用SDK后，在沙盒中生成的存储数据的文件夹，不同步到iCloud;<br/>
                                    2、自动登录流程优化;<br/>
                                    3、接收离线消息的回调接口有所调整，具体请参考<a href="http://www.easemob.com/docs/ios/releaseNote2_1_9">2.1.9release note</a>。 <br/>
                                    </span>
                                </dt>
                            </dl>
                        </li>
                        <li>
                            <h3><em></em><span>版本：V2.1.8 2015-06-19</span></h3>
                            <dl>
                                <dt>
                                    <span>新功能：<br/>
                                    1、支持不同网络类型间的实时音视频的互通(wifi/2G/3G/4G，beta版)。 <br/>
                                    </span>

                                    <span> SDK性能优化:<br/>
                                    1、从数据库获取EMMessage速度优化。<br/>
                                    </span>

                                    <span>SDK细节调整：<br/>
                                    1、EMError描述国际化：SDK提供EMError的中文和英文描述，默认为英文描述。 <br/>
                                    </span>
                                </dt>
                            </dl>
                        </li>
                        <li>
                            <h3><em></em><span>版本：V2.1.7 2015-05-28</span></h3>
                            <dl>
                                <dt>
                                    <span> bug fix:<br/>

                                    1、sdk的bug：登录后，免打扰群组列表获取有延迟；<br/>
                                    2、demo的bug：连续播放音频时可能crash；<br/>
                                    3、demo的bug：iPhone4上，点击重发按钮，重发按钮不会立刻消失。相应的修改代码在demo的重发操作里。<br/>
                                    </span>

                                    <span>新功能：<br/>
                                    1、聊天室，大家期待已久的聊天室上线了。 <br/>
                                    2、将语音的录制和播放相关代码从SDK中开源出来了，SDK不再管理相关代码，请开发者自由定制;<br/>
                                    3、请使用EaseMob单实例引用callManager. 在从2.1.7版本开始不会提供EMSDKFull及其头文件. EMSDKFull的功能将整合进EaseMob中;<br/>
                                    4、登录操作返回的错误码调整, 具体请参考<a href="http://www.easemob.com/docs/ios/releaseNote2_1_7">2.1.7release note</a>;<br/>
                                    5、支持分页获取公开群组。<br/>
                                    </span>
                                </dt>
                            </dl>
                        </li>
			      		<li>
                            <h3><em></em><span>版本：V2.1.6 2015-04-30</span></h3>
                            <dl>
                            <dt>
                                <span> 性能优化<br/>

                                1、优化wifi && 非rely环境下的实时语音接通率；<br/>
								 2、减小实时语音的静态库大小；<br/>
                                </span>
                                
                                <span>新功能：<br/>
								1、添加实时视频功能，beta版。需要在demo中添加依赖库libc++.dylib，实时视频不支持后台运行。 <br/>
								2、添加接口：离开群时是否自动删除群会话(Default is YES)，该接口的设置不会进行存储，需要开发者每次启动sdk之前设置一下
[[EaseMob sharedInstance].chatManager isAutoDeleteConversationWhenLeaveGroup];<br/>
								3、接口修改，具体请参考<a href="http://www.easemob.com/docs/ios/releaseNote2_1_6">2.1.6release note</a>.<br/>
								</span>
 
                            </dt>
                            </dl>
                        </li>
                        
                        	<li>
                            <h3><em></em><span>版本：V2.1.5 2015-04-08</span></h3>
                            <dl>
                            <dt>
                                <span>bug fix：<br/>

                                1、调用申请加入群组[applyJoinPublicGroup:]相关接口，有时会出现发送申请失败的情况；<br/>
								 2、调用[asyncUpdatePushOptions:]接口时, 未赋值的属性会被同步成默认值。<br/>
                                </span>
                                
                                <span>新功能：<br/>
                                1、判断当前socket是否连接。<br/>
                                </span>
                                
                                <span>细节调整：<br/>
                                1、Error列表整理，请使用Error的枚举声明进行判断，不要使用对应的数字编号；<br/>
								 2、EMCallManager文件结构整理。需要监听call相关的回调，请引用协议 EMCallManagerDelegate;<br/>
								 3、登陆成功之后，sdk内部不再自动获取群组列表，请自行调用。<br/>
								 </span>
                            </dt>
                            </dl>
                        </li>
                        
                        
			      		<li>
                            <h3><em></em><span>版本：V2.1.4 2015-03-14</span></h3>
                            <dl>
                            <dt>
                                <span>bug fix：<br/>
                                1、会话conversation数量很多的时候，偶尔会出现两条一样的;<br/>
                                2、群名称中包含“（”或者“）”，会造成crash;<br />
                                3、EMConversation.latestMessage.deliveryState值有时不对.<br/>
                                </span>	

                                <span>性能优化：<br/>
                                1、实时语音通话接通概率；<br/>
                                2、从数据库load conversation的速度.<br/>
                                </span>

                                <span>新功能：<br/>
                                1、自定义是否关闭打印的log，不能关闭log写入文件，目前我们需要log文件定位问题，望见谅；<br/>
                                2、添加DNS解析功能.<br/>
                                </span>
                            </dt>
                            </dl>
                        </li>
                        <li>
                            <h3><em></em><span>版本：V2.1.3r3 2015-02-04</span></h3>
                            <dl>
                            <dt>
                                <span>紧急修复：<br/>

                                1、ios2.1.3版本客户端创建群组，rest无法查到；<br/>
                                </span>
                            </dt>
                            </dl>
                        </li>

                        <li>
                            <h3><em></em><span>版本：V2.1.3r2 2015-02-02</span></h3>
                            <dl>
                            <dt>
                            <span>紧急修复：<br/>

                            1、覆盖安装自动登录失效；<br/>

                            2、只引用libEaseMobClientSDKLite.a会调用到libCallServer.a的方法，造成crash；<br/>
                            </span>
                            </dt>
                            </dl>
                        </li>

                        <li>
                        <h3><em></em><span>版本：V2.1.3 2015-01-31</span></h3>
                        <dl>
                            <dt>
                                <span>功能改进：<br/>

                                        1、优化登录操作；<br/>

                                        2、离线消息分为离线cmd消息和离线非cmd消息两种类型；<br/>

                                        3、因为安卓SDK暂时不支持多body，为了统一，IOS SDK请暂时不要使用多body的EMMessage结构。<br>
                                    <span>Bug Fix：<br/>
                                        1、修复：Database的数据存到了Document目录下，迁移到Library目录下；<br/>

                                        2、修复：特殊情况下，会出现收到离线消息的时候SDK中的Database还没有open, 造成第一条离线消息无法存进去;<br/>
                                    </span>
                                    <span>新功能：<br/>
                                        1、实时语音beta版。目前只支持wifi非relay情况下使用。如果想在黑屏状态或后台下能继续通话，请在工程里选择上"Voice over IP"或者“Audio and AirPlay”。</span>
                                </span>
                            </dt>
                        </dl>
                    </li>
			      	<li>
						<h3><em></em><span>版本：V2.1.2 2014-12-19</span></h3>
						<dl>
							<dt>
							    <span>功能改进：<br/>
							    
									1、需要新引入libsqlite3.dylib；<br/>
2、在登陆成功之后调用[importDataToNewDatabase]将数据导入新的数据库，使用示例:<br/>
		EMError *error = [[EaseMob sharedInstance].chatManager importDataToNewDatabase];
       if (!error) {
          error = [[EaseMob sharedInstance].chatManager loadDataFromDatabase];
       }；<br/>
3、检测工程中编译产生的所有error和warning，接口的更改会造成编译的失败或警告。<br/>
4、离线消息需要监听[didFinishedReceiveOfflineMessages:]回调方法，不会在[didReceiveMessage:]返回；<br/>
5、cmd类型的消息监听[didReceiveCmdMessage:]，不会在[didReceiveMessage:]返回<br/>
									
									替换快捷方法: <br/>
setp1、将旧的sdk从工程中删除，导入新的sdk；<br/>
setp2、编译工程，会出现一系列的warning;<br/>
setp3、将error和warning逐个击破，千万不要忽略warning，亲~~。<br/>
                                    Bug Fix：<br/>
									1、修复：附件默认下载状态。<br/>
									2、修复：设置自动登录，没网情况下启动app，再连网会自动进行重新登录。<br>
                                </span>
							</dt>
						</dl>
					</li>
			      	<li>
						<h3><em></em><span>版本：V2.1.1 2014-11-07</span></h3>
						<dl>
							<dt>
							    <span>功能改进：<br/>
							    
									1、发送透传消息（cmd类型），不存入数据库。<br/>
									
                                    Bug Fix：<br/>
									1、修复：群成员屏蔽群消息之后，无法退出群组。<br>
									2、修复：接收到的图片消息，大图的状态默认为undownload（旧版本默认为downloading）。<br>
                                </span>
							</dt>
						</dl>
					</li>
			      	<li>
						<h3><em></em><span>版本：V2.1.0 2014-10-18</span></h3>
						<dl>
							<dt>
							    <span>新功能/改进：<br/>
							    
									1、取消自动获取好友操作, 添加是否自动获取好友开关, 并添加手动获取好友列表API。<br/>
									2、透传功能：cmd类型的message。<br>
                                    Bug Fix：<br/>
									1、修复"自动登录过程中, 发送消息直接失败"的bug。<br>
									2、修复"断线重连过程中, 发送消息直接失败"的bug。<br>
									3、修复"APP被kill或者退出登录时, 正在发送的消息, 未标记为发送失败"的bug。<br>
									4、修复"APP被kill或者退出登录时, 正在获取的大图 download 状态, 未标记为 failed"的bug。<br/>
                                </span>
							</dt>
						</dl>
					</li>
			      	<li>
						<h3><em></em><span>版本：V2.0.9.1 2014-09-23</span></h3>
						<dl>
							<dt>
							    <span>紧急Bug Fix：<br/>
									紧急修复wifi 和 3G 切换时, 重连失败的bug
                                </span>
							</dt>
						</dl>
					</li>
			      	<li>
						<h3><em></em><span>版本：V2.0.9 2014-09-20</span></h3>
						<dl>
							<dt>
							    <span>新功能/改进：<br/>
							    
									1、屏蔽/取消屏蔽 群消息(服务器不发送消息)。<br/>
									2、添加消息送达回执。<br>
									3、本地缩略图显示模糊。<br>
                                    Bug Fix：<br/>
									1、消息附件下载状态修复。<br/>
                                </span>
							</dt>
						</dl>
					</li>
			      	<li>
						<h3><em></em>版本：V2.0.8 2014-08-28</h3>
						<dl>
							<dt>
							    <span>新功能/改进：<br/>
							    
									1、EMMessage中新添加了isOfflineMessage属性，在didReceiveMessage的时候， 可以根据是否为离线消息而决定是否重绘界面。
同时在offline message在接收过程中， 会有willReceiveOfflineMessages和didFinishedReceiveOfflineMessages：发出，用户可以根据此事件决定是否需要重绘UI。<br/>
									2、屏蔽群消息：接收并提醒 && 只接收不提醒。<br>
                                    Bug Fix：<br/>
									1、消息中的图片缩略图，在某些情况下，size.height为0。<br/>
									2、修正断线重连方面：切到后台，3分钟后，切回前台，有时会掉线的问题。<br/>
                                </span>
							</dt>
						</dl>
					</li>
					<div class="ios_ul">
						<li>
							<h3><em></em>版本：V2.0.7 2014-08-14</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
								    
										1、创建群组时，支持传最大成员数 EMGroupStyleSetting.groupMaxUsersCount，3 ~ 2000，ios默认是200；<br/>
										2、已创建的群组，获取详情时增加属性： 群组实际总人数和群组;<br/>
										3、添加 获取群组详情相关信息的接口;<br/>
										4、添加图片压缩比率开关 IChatImageOptions;<br/>
										5、后台发送纯文字信息（暂不支持发送图片），客户端正常显示。<br>
	                                    Bug Fix：<br/>
										1、创建群组时，invitees中去除创建者自己的username。<br/>
										 性能优化<br/>
										2、优化聊天记录搜索功能；<br/>
										3、优化聊天记录获取。<br/>
	                                </span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em>版本：V2.0.6 2014-07-31</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、好友黑名单<br/>
	                                    Bug Fix：<br/>
										1、修复了 登陆后设置消息推送昵称失败<br/>
	                                </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.5 2014-07-23</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、应用后台行为有播放音乐改成 background task
	                                    2、改进群组操作，提高易用性和速度<br/>
	                                    Bug Fix：<br/>
										1、修复了UI demo 里推送badge number 显示错误<br/>
	                                    2、修改200个conversation时出现的性能问题<br/>
	                                </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.4 2014-07-16</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、改进视频录制格式为MP4以和anroid 互通<br/>
	                                    Bug Fix：<br/>
										1、解决与ShareSDK等三方库的冲突问题<br/>
										2、解决群组在断网又恢复后出现的一些问题<br/>
	                                    3、解决后台删除用户在client端没有正确处理的问题<br/>
	                                    4、解决录音时锁屏的问题<br/>
	                                </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.3 2014-07-07</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、公开群支持用户申请群主批准入群<br/>
										2、支持群成员邀请其他用户入群<br/>
	                                    3、64位支持，XCode6 Beta2 适配<br/>
	                                    Bug Fix：<br/>
										1、修复Push 通知发送到多个设备的问题<br/>
										2、修复群组相关bugs<br/>
	                                </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.2 2014-07-01</h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、支持发送视频文件<br/>/br>
										2、支持自动登陆<br/>
	                                    Bug Fix：<br/>
										1、修复获取公开群相关的bug<br/>
										2、修复ChatDemo UI 上的重复对话项的bug<br/>
	                                </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.1 2014-06-25</h3>
							<dl>
								<dt>
								    <span>1、公开群组的支持<br/>
	                                    2、推送通知的支持<br/>
	                                    3、SDK里添加自动登录支持<br/>
	                                    4、bug fix<br/>
								    </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.0_GA 2014-06-17</h3>
							<dl>
								<dt>
								    <span>1、群聊功能隆重上线<br/>
	                                    2、完善errorCode, 错误处理更明确<br/>
	                                    3、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.0_beta6 2014-06-11</h3>
							<dl>
								<dt>
								    <span>1、优化断线重连功能<br/>
	                                    2、优化音频播放<br/>
	                                    3、优化消息发送队列和消息发送失败时的检测<br/>
	                                    4、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.0_beta5 2014-06-09</h3>
							<dl>
								<dt>
								    <span>1、UIDemo增加同一账号在不同手机上登录时踢出旧账号的功能<br />
								    	2、添加"被好友删除"时的回调通知<br />
								    	3、添加"好友请求被接受"时的回调通知<br />
	                                    4、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
	                    <li>
							<h3><em></em>版本：V2.0.0_beta4 2014-06-03</h3>
							<dl>
								<dt>
								    <span>1、添加聊天记录分页功能<br />
								    	2、添加音频播放动画<br />
								    	3、添加聊天消息和附件加密功能<br />
								    	4、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em>版本：V2.0.0_beta3 2014-05-16</h3>
							<dl>
								<dt>
								    <span>1、更新帮助文档<br />
								    	2、更新无UIdemo<br />
								    	3、更新有UIdemo<br />
								    	4、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em>版本：V2.0.0_beta2 2014-05-01</h3>
							<dl>
								<dt>
								    <span>1、更新帮助文档<br />
								    	2、更新无UIdemo<br />
								    	3、添加有UIdemo
								    </span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em>版本：V2.0.0_beta1 2014-04-25</h3>
							<dl>
								<dt>
								    <span>环信即时通讯云SDK V2.0重装上线。2.0是在1.0版基础上彻底的重写。更简洁易懂的API,更方便集成。<br />
								    </span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V 1.1.0 2014-01-08</span></h3>
							<dl>
								<dt>
								    <span>1、环信即时通讯云SDK 1.1.0上线啦。<br />
								    	2、say hello to Huanxin!<br />
								    </span>
								</dt>
							</dl>
						</li>
					</div>
					<li>
						<h3><em></em><a href="javascript:void(0);" class="ios_more" onclick="iosToggle()">更多……</a></h3>
					</li>
			    </ul>

			    <ul class="history_right">
				    <h2 class="first">Andriod SDK 更新日志</h2>
					<li>
	                    <h3><em></em><span>版本：V2.2.2 2015-08-05</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>	
							    1、支持Google push service,所以想做国际化APP的开发者可以用此版本
<br/>	
								2、修复日志输出导致的APPcrash
<br/>
								3、修复后台相应有问题时，前端导致的crash问题<br/>
								4、修复在弱网转态下，实时音视频卡顿的问题<br/>
								5、Demo集成parse SDK，展示如何获取联系人头像和昵称<br/>
								
						      </span>
						  </dt>
						</dl>
	                </li>     
				    <li>
	                    <h3><em></em><span>版本：V2.2.1 2015-07-03</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>	
							    1、提供新api，可以根据基本的消息类型分页获取消息EMChatManager.getMessagesByMsgType
<br/>	
								2、减小login timeout时间，避免弱网情况长时间login不返回
<br/>
								3、Demo增加环信助手演示功能，可自动回复消息<br/>
								
						      </span>
						  </dt>
						</dl>
	                </li>     
					<li>
	                    <h3><em></em><span>版本：V2.2.0 2015-06-15</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>	
							    1、支持不同网络类型间的实时音视频的互通(wifi/2G/3G/4G，beta版)<br/>	
								2、优化群同步时间，速度提升5倍<br/>
								3、新加API: EMConversation.getMessage(int position, boolean markAsRead)用来选择是否可以设置消息已读<br/>
								4、新加API: EMChat.setAppkey(String appkey)用来在代码里可以设置appkey<br/>
								5、优化demo登录体验，进到主页面加载群同步和联系人同步，用户体验大大提升<br/>
						        6、优化demo国际化
						      </span>
						  </dt>
						</dl>
	                </li>     
					<li>
	                    <h3><em></em><span>版本：V2.1.9 2015-05-23</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>	
							    1、增加聊天室模型<br/>	
								2、增加分页获取公开群API<br/>
								3、优化音视频，提高接通率，和接通速度<br/>
								4、改进收到离线消息时的震动提示以及UI刷新<br/>
								5、其他内部优化<br/>
						         Bug Fix：<br/>
						        1、修复demo将联系人移入黑名单的时候程序可能crash的问题<br/>		
						        2、修复demo进入群详情页面，应用可能crash的问题<br/>
						        3、修复demo某些情况下主界面未读消息不刷新的问题<br/>
						      </span>
						  </dt>
						</dl>
	                </li>     
					<li>
	                    <h3><em></em><span>版本：V2.1.8r2 2015-04-30</span></h3>
						<dl>
						  <dt>
						      <span>	
							    修复前一个版本在某些情况下会导致卡ui的问题
						      </span>
						  </dt>
						</dl>
	                </li>    
					<li>
	                    <h3><em></em><span>版本：V2.1.8 2015-04-17</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>	
							    1、提供新API回调接口用来替换broadcast的通知回调，并且把消息震动、响铃、通知栏提醒等操作提出到demo中，这样app可以更灵活的定制收到消息时的处理，例如可以实现免打扰功能，定制个性化通知等等 **具体可以参考函数EMChatManager.registerEventListener, 和UIDemo里的代码实现**<br/>	
								2、新增守护进程，提高app放在后台一段时间后不被杀死的概率，** APP 需要把libeasemobservice.so复制到相应的lib目录下**<br/>
								3、增加批量导入的接口EMChatManager.importMessages<br/>
						         Bug Fix：<br/>
						        1、修复群主踢人，APP收不到被踢通知的问题<br/>		
						        2、修复发送透传CMD消息时，在没有ext字段时，消息反序列化出错的问题，这样会导致APP收不到CMD消息<br/>
						        3、修复发送透传CMD消息时，获取不到JSONObject 或者 JSONArray 对象的问题<br/>
								4、修复上一个版本的demo可能无法拉取更多消息的问题
						      </span>
						  </dt>
						</dl>
	                </li>     
					 <li>
	                    <h3><em></em><span>版本：V2.1.7 2015-03-31</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、改进从数据库load conversation的速度，对于大量消息数据和大量会话的情况加速明显<br/>	
								2、优化获取好友，获取速度更快及更省流量<br/>
								3、删除会话时可以选择不删除消息<br/>
						         Bug Fix：<br/>
						        1、修复瞬时接收大量消息时app可能crash的问题<br/>		
						        2、修复readAck & deliverAck丢包问题<br/>
						        3、修复某些情况下不能删除好友以及获取的好友列表不对的问题<br/>
						      </span>
						  </dt>
						</dl>
	                </li>     
					 <li>
	                    <h3><em></em><span>版本：V2.1.6 2015-03-06</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、增加扩展属性支持JsonObject和JsonArray<br/>
						        2、增加新API EMChat:isLoggedIn()用来查询是否登录过<br/>					        
						         Bug Fix：<br/>
						        1、修复DNS解析错误<br/>		
						        2、修复实时音视频电话遇到的状态出错的问题<br/>
						        3、修复一个群消息被错误删除的问题<br/>
						        4、修复点击文件消息头像出现的null pointer问题<br/>
								5、修复demo录像时有时候出现闪退的问题</br>
						      </span>
						  </dt>
						</dl>
	                </li>     
					 <li>
	                    <h3><em></em><span>版本：V2.1.5 2015-01-31</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、增加实时视频通话(Beta)<br/>
						        2、为了减少登录时间，SDK默认现在是不会去取黑名单，如果需要，请app自己去获取,可参考demo的LoginActivity<br/>
						        3、由于增加视频电话的功能，so文件有些更改（之后也有可能会更改），请之前用到语音电话的app更改下<br/>						        
						         Bug Fix：<br/>
						        1、修复偶尔重连时，导致ANR的问题<br/>		
						        2、修复成员数量超过最大成员数时，没有异常抛出的问题<br/>
						        3、修复收到消息时，无法解析body里的Json数组的问题<br/>
						        4、修复小米手机有时候收到消息时持续震动的问题<br/>
								5、修复修复屏蔽群消息后，收不到被踢的通知的问题<br/>
								6、修复屏蔽群后，无法退群的问题<br/>
								 
						      </span>
						  </dt>
						</dl>
	                </li>     
				    <li>
	                    <h3><em></em><span>版本：V2.1.4 r2 2015-01-07</span></h3>
						<dl>
						  <dt>
						         Bug Fix：<br/>
						        &nbsp;&nbsp;修复已经登录成功再次登录失败的问题
<br/> &nbsp;&nbsp;修复屏蔽群后，不能退出群聊的问题
<br/>
						      </span>
						  </dt>
						</dl>
	                 </li> 
				    <li>
	                    <h3><em></em><span>版本：V2.1.4 2014-12-31</span></h3>
						<dl>
						  <dt>
						      <span>sdk 更新：<br/>
						       &nbsp;&nbsp;1.加快重连<br/>
						       &nbsp;&nbsp;2.优化登录<br/>
						       &nbsp;&nbsp;3.增加error EMError.USER_REMOVED,用来通知当前用户被移除<br/>
						        demo app 更新：<br/>
                                &nbsp;&nbsp;更新百度sdk最新版<br/>
						         Bug Fix：<br/>
						        &nbsp;&nbsp;修复小米手机来消息一直震动的问题
<br/>
						      </span>
						  </dt>
						</dl>
	                 </li> 
				    	<li>
	                    <h3><em></em><span>版本：V2.1.3 2014-11-28</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        新加API：<br/>&nbsp;EMChatManager.deleteAllConversation()<br/>
						        &nbsp;EMChatManager.resetAllUnreadMsgCount()<br/>
						        &nbsp;EMGroupManager.asyncGetGroupsFromServer<br/>
						        &nbsp;EMGroupManager.asyncGetAllPublicGroupsFromServer
<br/>
						        &nbsp;增加异步logout(EMCallBack callback) 调用<br/>
						        demo app 更新<br/>
                                &nbsp;在其他页面，增加消息通知显示<br/>
                                &nbsp;封装一些和环信初始化相关的类(HXSDKHelper)<br/>
                                &nbsp;减小图像压缩比率使接收图像更清晰<br/>
						         Bug Fix：<br/>
						        &nbsp;1、在某些情况下，直接调用logout 导致异常<br/>
						        &nbsp;2、多次login，回调不返回<br/>
						      </span>
						  </dt>
						</dl>
	                 </li> 
				      <li>
	                    <h3><em></em><span>版本：V2.1.2 2014-11-07</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、增加error code EMError类，方便开发者查询返回值<br/>
						        2、增加EMChatManager.loadAllConversations() 和EMGroupManager.loadAllGroups 去主动加载会话列表和群组 <br/>
						        **请注意，请在app初始化界面调用此api一次即可，可参考demo（login and splash activity）<br/>
						        3、通讯录中过滤黑名单<br/>
						        4、优化录制视频清晰度、调整录制方向，添加录制视频时间、视频前后摄像头切换(UIDemo)<br/>
						        5、录音添加权限检测(UIDemo)<br/>
						        6、新增监听接口EMConnectionListener 用来替换ConnectionListener<br/>        
						        7、新增更新消息内容接口EMChatManager.getInstance().updateMessageBody({emmessage})<br/>
						        8、透传消息添加群聊支持<br/>
						         Bug Fix：<br/>
						        &nbsp;1、送达通知无法显示<br/>
						        &nbsp;2、消息界面无法显示接收消息，只能听到声音，UIDemo问题<br/>
						      </span>
						  </dt>
						</dl>
	                </li>  
				     <li>
	                    <h3><em></em><span>版本：V2.1.1 2014-10-18</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、增加透传功能<br/>
						        2、优化重连<br/>
						        3、提供具体error code 码，可以参考EMCallBack<br/>
						        4、增强稳定性<br/>
						        5、登录取消取环信好友列表(<strong>注意* 如果app还想用环信好友列表可以在初始化环信时调用此方法options.setUseRoster(true);</strong>)<br/>
						        过时的类通知：<br/>
						        &nbsp;&nbsp;<strong>EMChatDB ： 此类将在后续版本中去掉，请注意</strong><br/>
						      </span>
						  </dt>
						</dl>
	                </li>      
				     <li>
	                    <h3><em></em><span>版本：V2.1.0 2014-09-30</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、断网发图片增加等待时间，不会立即停止发送<br/>
						        2、优化取离线消息,多次通知改一次通知<br/>
						        3、添加接收语音文件名可以显示扩展名的配置<br/>
						        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如：chatOptions.setAudioFileWithExt(true)<br/>
						         Bug Fix：<br/>
						        1、修复下载图片偶尔失败的问题<br/>		
						        2、修复自动重连失败的问题<br/>
						        3、修复账号在其他地方登陆问题<br/>
						        4、修复偶尔发不出去消息的问题<br/>
								 
						      </span>
						  </dt>
						</dl>
	                </li>      
	                <li>
	                    <h3><em></em><span>版本：V2.0.9 2014-09-15</span></h3>
						<dl>
						  <dt>
						      <span>新功能/改进：<br/>
						        1、新增实时语音（BETA版,现支持wifi和wifi之间的通话，手机3G/2G/4G间通话暂时不支持，下一版本会支持）<br/>
						        2、新增消息送达通知<br/>
						        3、新增屏蔽群消息功能<br/>			
						         Bug Fix：<br/>
						        1、修复群组多次连着加人踢人收不到消息的bug<br/>		
						        2、修复并发取未读消息时并发异常错误<br/>
						        3、修复logger null pointer 异常错误<br/>
								 注意：<br/>
								1、新版本对db做了一点改动，覆盖安装时需要app把清单文件的version加大<br/>
								2、增加一个语音通话所需要的so库文件，如需使用语音通话功能引用下载的压缩包里libs底下的文件，不需要此功能则引入libs.without.audio里面的jar文件即可<br/>
						      </span>
						  </dt>
						</dl>
	                </li>      
	                <li>
			            <h3><em></em><span>版本：V2.0.8 2014-08-30</span></h3>
		                <dl>
		                  <dt>
		                    <span>新功能/改进：<br/>
		                      1、优化了token 的获取和更新<br/>
		                      2、优化了在 wifi 环境下的长连接维护部分<br/>
		                      3、支持设置用户昵称，ios APNS 推送的时候能显示此名称<br/>
		                      4、EMChatConfig.getInstance().AccessToken的调用方式改成EMChatManager.getInstance().getAccessToken()<br/>
		                      5、支持消息notification提示时修改通知的标题<br/>									
		                       Bug Fix：<br/>
		                      1、修复了有些情况下网络切换无法自动重连的问题<br/>		
		                      2、修复了消息中包含某些特殊字符时接收到内容不一致的问题<br/>
		                      3、修复了concurrent access conversation 的问题<br/>
		                    </span>
		                  </dt>
		                </dl>
		            </li>
					<div class="andriod_ul">
						<li>
						    <h3><em></em><span>版本：V2.0.7 2014-08-19</span></h3>
							<dl>
								<dt>
									<span>新功能/改进：<br/>
										1、加入了log 文件。环信sdk的debug 信息会存储到log文件<br/>
										2、加入群组成员限制，群组人数达到最大限制时不让再加<br/>
										3、demo更新支持显示非联系人<br/>
										4、优化的聊天窗口里图片的显示<br/>
										5、demo文字消息支持网页链接提示<br/>									
										 Bug Fix：<br/>
										1、修复了再次进入应用，未读数显示不对的问题<br/>		
										2、修复了离线消息的时间问题<br/>
										3、修复在某些机型上不能收发文件及视频消息的bug<br/>
									</span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V2.0.6 2014-08-01</span></h3>
							<dl>
								<dt>
									<span>新功能/改进：<br/>
										1、黑名单功能<br/>
										2、创建群组支持设置群最大用户数以及获取群组成员数<br/>
										3、支持导入自己的消息<br/>
										4、支持群组消息设成只显示数目不提示消息<br/>
										5、优化群组查询<br/>
										6、其他小的API及优化<br/>										
										 Bug Fix：<br/>
										1、修复一次性发送多张图片消息，显示发送的数目不对的问题<br/>		
										2、修复发送图片语音等文件消息过慢的问题<br/>
									</span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V2.0.5 2014-07-23</span></h3>
							<dl>
								<dt>
									<span>新功能/改进：<br/>
										1、demo及sdk支持收发文件消息<br/>
										2、demo提供视频录制<br/>
										3、Text Message支持json数据做为message body<br/>
										4、sdk支持username使用大写字母，sdk会自动转为小写<br/>
										 Bug Fix：<br/>
										1、修复有时候语音无法播放的问题<br/>
										2、修复UI demo上连接状态有时候显示不对的问题<br/>
										3、修复自定义通知内容, 有时候不管用的问题<br/>				
									</span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V2.0.4 2014-07-16</span></h3>
							<dl>
								<dt>
									<span>新功能/改进：<br/>
										1、合并jar 文件，简化安装包。环信sdk只需要一个 easemobchatsdk.jar<br/>
										2、增大http 操作的超时时间以适应弱网络情况<br/>
										3、显示语音消息下载进度，下载成功才可以播放<br/>
										4、优化EMChatService<br/>
										 Bug Fix：<br/>
										1、修复了断网情况下收不到群组邀请和群组删除消息的问题<br/>
										2、修复了有些情况的网络切换后没有自动重连到服务器的问题<br/>
										3、修复了公开群离线被踢收不到回调的bug<br/>					
									</span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V2.0.3 2014-07-07</span></h3>
							<dl>
								<dt>
									<span>新功能/改进：<br/>
										1、公开群支持用户申请群主批准入群<br/>
										2、支持发送视频文件<br/>
										3、android 和 iOS 表情互通<br/>
										 Bug Fix：<br/>
										1、修复大小写用户登陆无法发消息的问题<br/>
										2、修复加入，退出公开群相关的几个问题<br/>
										3、修复公开群显示乱码问题<br/>							  
									</span>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V2.0.2 2014-06-30</span></h3>
							<dl>
								<dt>
								    <span>新功能/改进：<br/>
										1、群组增加选项允许成员邀请其他用户入群<br/>
										2、增大socket timeout时间<br/>
										3、改变 intent action 特殊字符以支持在AndroidManifest 里面声明message receiver<br/>
										4、SDK 支持开机自启动，并修改UI demo<br/>
										5、支持开发者自定义 notification intent 的行为<br/>
										6、发送接收文件改成使用https<br/>
										 Bug Fix：<br/>
										1、修复加入退出公开群组的相关bug<br/>
										2、修复UI 连接状态显示bug<br/>
										3、修复离线添加好友问题<br/>

								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.1 2014-06-22</span></h3>
							<dl>
								<dt>
								    <span>1、A断网后,群主把A踢出群。A连网后，还有此群，在群里发消息，显示发送失败<br/>
								    2、加好友时好友同意了,有时好友列表里没有此好友<br/>
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_GA 2014-06-11</span></h3>
							<dl>
								<dt>
								    <span>1、UIDemo增加群聊功能。
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_beta5 2014-06-09</span></h3>
							<dl>
								<dt>
								    <span>1、UIDemo增加同一账号在不同手机上登录时踢出旧账号的功能<br />
								    	2、UIDemo修复消息回执的已读状态的自动刷新问题<br />
								    	3、UIDemo添加好友，如果对方已经是好友，应该提醒“XXX已经是您的好友”。<br/>
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_beta4 2014-06-03</span></h3>
							<dl>
								<dt>
								    <span>1、修复发送添加好友邀请后，如果对方忽略请求，对方会在每次上线后重复收到请求的bug<br />
								    	2、UIDemo增加扬声器播放声音选项。<br />
								    	3、修复小米联想手机上语音播放控件的选中状态问题。<br/>
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_beta3 2014-05-26</span></h3>
							<dl>
								<dt>
								    <span>1、把缺省UI模板改为彩色”时尚版“。但同时也将会提供别的风格（目前有企业版）提供下载。多处UI改进。我们的目标不是提供一个demo演示，而是提供一个产品级别的完整聊天产品的源码。让大家拿去就能用
									<br />
								    	2、无SD卡时拍照闪退fix。<br />
								    	3、文档增加声音，震动控制说明。<br/>
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_beta2 2014-05-16</span></h3>
							<dl>
								<dt>
								    <span>1、更新帮助文档<br />
								    	2、更新无UIdemo<br />
								    	3、更新有UIdemo<br />
								    	4、bug fixes
								    </span>
								</dt>
							</dl>
						</li>
				      	<li>
							<h3><em></em><span>版本：V2.0.0_beta1 2014-05-01</span></h3>
							<dl>
								<dt>
								    <span>1、更新帮助文档<br />
								    	2、更新无UIdemo<br />
								    	3、添加有UIdemo
								    </span>
								</dt>
							</dl>
						</li>
					    <li>
					    	<h3><em></em><span>版本：V2.0.0_alpha1 2014-04-25</span></h3>
					    	<dl>
							<dt>
							    <span>环信即时通讯云SDK V2.0重装上线。2.0是在1.0版基础上彻底的重写。更简洁易懂的API,更方便集成。<br />
							    </span>
							</dt>
						    </dl>
					    </li>
						<li>
							<h3><em></em><span>版本：V 1.1.0 2014-01-08</span></h3>
							<dl>
								<dt>
								    <span>1、环信即时通讯云SDK 1.1.0上线啦。<br />
								    	2、say hello to Huanxin!<br />
								    </span>
								</dt>
							</dl>
						</li>
					</div>
					<li>
						<h3><em></em><a href="javascript:void(0);" class="andriod_more" onclick="andriodToggle()"><span>更多……</span></a></h3>
					</li>
		        </ul>
			    <ul class="history_left history_margin_right">
			      	<h2 class="first">WebIM SDK 更新日志</h2>
					<li>
							<h3><em></em><span>版本：V1.0.5 2015-3-11</span></h3>
							<dl>
								<dt>
								 <span>新功能：<br/>
			  1、优化底层连接，减少系统登录耗时<br/>
			  2、添加透传消息支持（注册onCmdMessage事件，以监听服务器端推送的透传消息）<br/>
			  3、添加收到消息后，自动发送回复消息给服务器<br/>
			  4、当图片下载失败时默认再一次下载<br/></span>
								</dt>
								<dt>
								</dt>
							</dl>
						</li>
						<li>
							<h3><em></em><span>版本：V1.0.4.1 2015-1-15</span></h3>
							<dl>
								<dt>
								 <span>新功能：<br/>
			  1、收到文件消息通知，暂不支持下载<br/>
			  2、收到视频消息通知，暂不支持下载<br/></span>
								</dt>
								<dt>
								    <span>Bug Fix：<br/>1、修复bug <br/>
		修复不点击‘退出’按钮直接关闭浏览器下次登录消息丢失的bug<br/>
			                        </span>
								</dt>
							</dl>
						</li>
			      		<li>
							<h3><em></em><span>版本：V1.0.4 2014-12-17</span></h3>
							<dl>
								<dt>
								    <span>Bug Fix：<br/>1、修复bug <br/>
		群聊位置消息作为单聊消息处理<br/>
			  2、修改bug <br/>
		好友列表为空时陌生人消息不显示<br/>
	                                </span>
								</dt>
							</dl>
						</li>
			      	<li>
						<h3><em></em><span>版本：V1.0.3 2014-12-11</span></h3>
						<dl>
							<dt>
							    <span>新功能：<br/>
							    
									1、增加陌生人聊天功能<br/>
									2、添加新用户注册功能<br>
                                    3、支持https访问模式<br/>
									4、支持token登录<br/>
									5、支持语音消息<br/>
									6、消息体支持自定义扩展,添加ext属性<br/>
                                    7、demo示例支持未读消息提醒<br/>
                                </span>
								<br>
	
								<span>功能改进：<br/>
							    
									1、修复bug <br/>demo联系人过多时的样式问题<br/>
									2、修复bug <br/>conn = new Easemob.im.Connection();变量名不为conn或者conn不是全局变量时接受不到消息<br>
                                    3、修复bug <br/>群组离线消息当作陌生人消息处理<br/>
									4、修复bug <br/>IE浏览器接受文本消息以换行符开始时会遮挡联系人名称<br/>
									5、修复bug <br/>在线用户被邀请加入群组不能实时显示，必须重新登录<br/>
									6、丰富相关文档内容<br/>
                                </span>
							</dt>
						</dl>
					</li>
					<!-- <li>
						<h3><em></em><a href="javascript:void(0);" class="web_more" onclick="webToggle()"><span>更多……</span></a></h3>
					</li> -->
				</ul>
		    </div>
			<script type="text/javascript">
				function iosToggle(){
				    $(".ios_ul").slideToggle(2000);//窗帘效果的切换,点一下收,点一下开,参数可以无,参数说明同上
				    $(".ios_more").hide();
				}
				function andriodToggle(){
				    $(".andriod_ul").slideToggle(2000);//窗帘效果的切换,点一下收,点一下开,参数可以无,参数说明同上
				    $(".andriod_more").hide();
				}
				function webToggle(){
				    $(".web_ul").slideToggle(2000);//窗帘效果的切换,点一下收,点一下开,参数可以无,参数说明同上
				    $(".web_more").hide();
				}
			</script>
		</div>
	</div>
	<div class="clearfix"></div>
</div>

