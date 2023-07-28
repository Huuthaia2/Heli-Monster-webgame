!function () {
        "use strict";

        class t extends Laya.Script {
            constructor() {
                super(), this.scale = 0, this.moveTime = 100, this.state = "", this.finalPosition = new Laya.Vector3(0, 0, 0), this.RandomX = 0, this.RandomY = 0
            }

            Init(t, i, e, a) {
                this.data = t, this.owner.scaleX = this.scale, this.owner.scaleY = this.scale, 1 == e && (this.RandomX = D.RandomFloat(-50, 50), this.RandomY = D.RandomFloat(-100, 100)), Laya.Tween.to(this.owner, {
                    x: this.owner.x + this.RandomX,
                    y: this.owner.y + this.RandomY,
                    scaleX: a,
                    scaleY: a
                }, 300, null, null, this.data.delay), Laya.timer.frameOnce(30, this, function () {
                    Laya.Tween.to(this.owner, {
                        x: this.data.target.x,
                        y: this.data.target.y,
                        scaleX: 1,
                        scaleY: 1
                    }, 300, null, null, this.data.delay)
                }), Laya.timer.frameOnce(50, this, function () {
                    Laya.Tween.to(this.owner, {
                        x: this.data.target.x,
                        y: this.data.target.y,
                        scaleX: .5,
                        scaleY: .5
                    }, 30, null, Laya.Handler.create(this, function () {
                        null != i && i(), this.owner.destroy()
                    }), this.data.delay)
                })
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        var i = Laya.View,
            e = (Laya.Dialog, Laya.Scene),
            a = Laya.ClassUtils.regClass;

        class o extends i {
            constructor() {
                super()
            }

            createChildren() {
                super.createChildren(), this.createView(o.uiView)
            }
        }

        o.uiView = {
            type: "View",
            props: {
                zOrder: 12,
                width: 720,
                height: 1280
            },
            compId: 2,
            child: [{
                type: "Image",
                props: {
                    y: 0,
                    x: 0,
                    width: 684,
                    skin: "UIRes/repeat/Image_repeat_03.png",
                    pivotY: 49,
                    pivotX: 342,
                    height: 97
                },
                compId: 5,
                child: [{
                    type: "Label",
                    props: {
                        width: 400,
                        var: "value",
                        valign: "middle",
                        text: "Not enough coins",
                        height: 67,
                        fontSize: 30,
                        font: "Microsoft YaHei",
                        color: "#ffffff",
                        centerY: 6,
                        centerX: 0,
                        bold: !0,
                        align: "center"
                    },
                    compId: 4
                }]
            }],
            animations: [{
                nodes: [{
                    target: 5,
                    keyframes: {
                        y: [{
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 5,
                            key: "y",
                            index: 0
                        }, {
                            value: -50,
                            tweenMethod: "linearOut",
                            tween: !0,
                            target: 5,
                            key: "y",
                            index: 90
                        }],
                        alpha: [{
                            value: 1,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 5,
                            key: "alpha",
                            index: 0
                        }, {
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 5,
                            key: "alpha",
                            index: 90
                        }]
                    }
                }],
                name: "ani1",
                id: 1,
                frameRate: 24,
                action: 1
            }],
            loadList: ["UIRes/repeat/Image_repeat_03.png"],
            loadList3D: []
        }, a("ui.UIPanel.GameTipUI", o);

        class n extends e {
            constructor() {
                super()
            }

            createChildren() {
                super.createChildren(), this.createView(n.uiView)
            }
        }

        n.uiView = {
            type: "Scene",
            props: {
                width: 720,
                height: 1280
            },
            compId: 2,
            child: [{
                type: "Label",
                props: {
                    var: "showNum",
                    text: "1",
                    font: "font03",
                    anchorY: .5,
                    anchorX: .5
                },
                compId: 3
            }],
            animations: [{
                nodes: [{
                    target: 3,
                    keyframes: {
                        y: [{
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "y",
                            index: 0
                        }, {
                            value: -20,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "y",
                            index: 10
                        }],
                        x: [{
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "x",
                            index: 0
                        }, {
                            value: -39,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "x",
                            index: 10
                        }],
                        alpha: [{
                            value: 1,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "alpha",
                            index: 0
                        }, {
                            value: 1,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "alpha",
                            index: 10
                        }, {
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "alpha",
                            index: 15
                        }]
                    }
                }],
                name: "ani1",
                id: 1,
                frameRate: 24,
                action: 0
            }, {
                nodes: [{
                    target: 3,
                    keyframes: {
                        y: [{
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "y",
                            index: 0
                        }, {
                            value: -20,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            label: null,
                            key: "y",
                            index: 10
                        }],
                        x: [{
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "x",
                            index: 0
                        }, {
                            value: 39,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            label: null,
                            key: "x",
                            index: 10
                        }],
                        alpha: [{
                            value: 1,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "alpha",
                            index: 0
                        }, {
                            value: 1,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            label: null,
                            key: "alpha",
                            index: 10
                        }, {
                            value: 0,
                            tweenMethod: "linearNone",
                            tween: !0,
                            target: 3,
                            key: "alpha",
                            index: 15
                        }]
                    }
                }],
                name: "ani2",
                id: 2,
                frameRate: 24,
                action: 0
            }],
            loadList: [],
            loadList3D: []
        }, a("ui.UIPanel.PreJiaShuUIUI", n);

        class s extends Laya.Script3D {
            constructor() {
                super(), this.scale = 0, this.moveTime = 10, this.state = "", this.finalPosition = new Laya.Vector3(0, 0, 0)
            }

            Init(t) {
                this.data = t, this.thisTrans = this.owner.transform, this.moveY = 0, this.thisTrans.setWorldLossyScale(new Laya.Vector3(this.scale, this.scale, this.scale)), this.finalPosition = this.thisTrans.position.clone(), this.moveX = this.thisTrans.position.x + D.RandomFloat(-4, 4), this.moveZ = this.thisTrans.position.z + D.RandomFloat(-4, 4), this.thisTrans.localRotationEuler = new Laya.Vector3(D.RandomFloat(0, 360), D.RandomFloat(0, 360), 0), this.state = "create"
            }

            onUpdate() {
                switch (this.state) {
                    case "create":
                        if (this.data.delay -= 1, this.data.delay <= 0) {
                            this.scale = .6, this.thisTrans.setWorldLossyScale(new Laya.Vector3(this.scale, this.scale, this.scale));
                            var t = .1;
                            null == this.fanzhuan ? (this.moveY += this.GetDir(7 - this.moveY) * t, this.moveY >= 6 && (this.fanzhuan = !0), this.finalPosition.x += this.GetDir(this.moveX - this.finalPosition.x) * t * .3, this.finalPosition.z += this.GetDir(this.moveZ - this.finalPosition.z) * t * .3) : (this.moveY += this.GetDir(0 - this.moveY) * t, this.moveY <= 0 && (this.moveY = 0), this.finalPosition.x += this.GetDir(this.moveX - this.finalPosition.x) * t * 2, this.finalPosition.z += this.GetDir(this.moveZ - this.finalPosition.z) * t * 2), this.thisTrans.position = new Laya.Vector3(this.finalPosition.x, this.moveY, this.finalPosition.z), this.thisTrans.localRotationEulerX += this.GetDir(0 - this.thisTrans.localRotationEulerX) * t * .5, this.thisTrans.localRotationEulerY += this.GetDir(0 - this.thisTrans.localRotationEulerY) * t * .5, this.thisTrans.localRotationEulerZ += this.GetDir(0 - this.thisTrans.localRotationEulerZ) * t * .5, this.moveTime -= t, this.moveTime <= 0 && (this.finalPosition = this.thisTrans.position.clone(), this.state = "move")
                        }
                        break;
                    case "move":
                        t = .1;
                        var i = new Laya.Ray(new Laya.Vector3(0, 0, 0), new Laya.Vector3(0, 0, 0));
                        i = new Laya.Ray(new Laya.Vector3(0, 0, 0), new Laya.Vector3(0, 0, 0)), D.mainCamera.viewportPointToRay(new Laya.Vector2(607, 230), i);
                        var e = new Laya.Vector3(0, 0, 0);
                        if (Laya.Vector3.scale(i.direction, 30, e), Laya.Vector3.add(D.mainCamera.transform.position, e, e), this.finalPosition.x += this.GetDir(e.x - this.finalPosition.x) * t * 2, this.finalPosition.y += this.GetDir(e.y - this.finalPosition.y) * t * 2, this.finalPosition.z += this.GetDir(e.z - this.finalPosition.z) * t * 2, this.thisTrans.position = new Laya.Vector3(this.finalPosition.x, this.finalPosition.y, this.finalPosition.z), this.scale += .03 * (.1 - this.scale), this.thisTrans.setWorldLossyScale(new Laya.Vector3(this.scale, this.scale, this.scale)), this.scale <= .4) return this.owner.destroy(), void (this.state = "over")
                }
            }

            GetDir(t) {
                return t
            }
        }

        class r {
            static ShowUIPanel(t, i = !0, e = null) {
                Laya.Scene.open("UIPanel/" + t + ".scene", i, e)
            }

            static createGoldEffect(t) {
                var i = Laya.stage.width,
                    e = Laya.stage.height;
                if (window.qg) {
                    var a = qg.getSystemInfoSync();
                    i = a.screenWidth, e = a.screenHeight
                }
                var o = new Laya.Ray(new Laya.Vector3(0, 0, 0), new Laya.Vector3(0, 0, 0));
                D.mainCamera.viewportPointToRay(new Laya.Vector2(.5 * i, .5 * e), o);
                var n = new Laya.Vector3(0, 0, 0);
                Laya.Vector3.scale(o.direction, 30, n), Laya.Vector3.add(D.mainCamera.transform.position, n, n), Laya.Vector3.subtract(n, D.cameraTrans.transform.position, n), o = new Laya.Ray(new Laya.Vector3(0, 0, 0), new Laya.Vector3(0, 0, 0)), D.mainCamera.viewportPointToRay(new Laya.Vector2(48, 97), o);
                var r = new Laya.Vector3(0, 0, 0);
                Laya.Vector3.scale(o.direction, 30, r), Laya.Vector3.add(D.mainCamera.transform.position, r, r), Laya.Vector3.subtract(r, D.cameraTrans.transform.position, r);
                for (var h = 0; h < t; h++) {
                    var l = Laya.Sprite3D.instantiate(D.models.getChildByName("money"), D.curScene);
                    l.transform.position = D.cameraTrans.transform.position.clone(), l.addComponent(s).Init({
                        delay: h * (50 / t),
                        target: {
                            x: r.x,
                            y: r.y,
                            z: r.z
                        }
                    }), l.layer = 1
                }
            }

            static ShowGameTipUI(t) {
                var i = new Laya.Point(360, 700);
                let e = Laya.stage.addChild(new o);
                e.value.text = t, e.x = i.x, e.y = i.y, Laya.timer.frameOnce(120, this, function () {
                    e.destroy()
                })
            }

            static ShowPreJiaYiUI(t, i, e) {
                let a = Laya.stage.addChild(new n);
                var o = new Laya.Vector4;
                D.mainCamera.worldToViewportPoint(i, o), a.showNum.font = 1 == e ? "font04" : "font03", a.showNum.text = t, D.RandomInt(0, 11) < 5 ? a.ani1.play(0, 0) : a.ani2.play(0, 0), a.x = o.x, a.y = o.y, Laya.timer.frameOnce(120, this, function () {
                    a.destroy()
                })
            }

            static CreateGoldEffectUI(i, e, a, o, n) {
                for (var s = 0; s < i; s++) {
                    var r = new Laya.Image("UIRes/game/Image_game_" + e + ".png");
                    r.anchorX = .5, r.anchorX = .5, Laya.stage.addChild(r), r.zOrder = -1;
                    var h = new Laya.Vector4;
                    D.mainCamera.worldToViewportPoint(n, h), r.x = h.x, r.y = h.y - 50, r.addComponent(t).Init({
                        delay: s * (50 / i),
                        target: {
                            x: a,
                            y: o
                        }
                    }, null, !1, 2)
                }
            }

            static CreateGoldEffectCoinUI(i, e, a, o) {
                for (var n = 0; n < i; n++) {
                    var s = new Laya.Image("UIRes/repeat/Image_repeat_04.png");
                    s.anchorX = .5, s.anchorX = .5, Laya.stage.addChild(s);
                    var r = new Laya.Vector4;
                    D.mainCamera.worldToViewportPoint(o, r), s.x = r.x, s.y = r.y - 150, s.addComponent(t).Init({
                        delay: n * (50 / i),
                        target: {
                            x: e,
                            y: a
                        }
                    }, null, !0, 1)
                }
            }
        }

        r.gameUI = null, r.joy = null, r.pushUI = 0;

        class h {
            static GetData() {
                var t = Laya.LocalStorage.getItem("mlzxData");
                t && (h.user = JSON.parse(t))
            }

            static SaveData() {
                var t = JSON.stringify(h.user);
                Laya.LocalStorage.setItem("mlzxData", t)
            }

            static GetUserData(t) {
                return null != h.user[t] ? h.user[t] : h.userDV[t]
            }

            static SetUserData(t, i) {
                h.user[t] = i, h.SaveData()
            }

            static AddProp(t, i) {
                1 == t ? h.SetUserData("Gold", h.GetUserData("Gold") + i) : 2 == t && h.SetUserData("Money", h.GetUserData("Money") + i)
            }

            static IsCanLessProp(t, i) {
                if (1 == t) {
                    if (h.GetUserData("Gold") >= i) return !0
                } else if (2 == t && h.GetUserData("Money") >= i) return !0;
                return !1
            }

            static LessProp(t, i) {
                var e = 0;
                1 == t ? (e = h.GetUserData("Gold")) >= i && h.SetUserData("Gold", e - i) : 2 == t && (e = h.GetUserData("Money")) >= i && h.SetUserData("Money", e - i)
            }

            static SavePiFuTypeList(t) {
                var i = h.GetUserData("piFuType");
                i[t] = 1, h.SetUserData("piFuType", i)
            }

            static savePiFuTypeNum(t) {
                h.SetUserData("piFuTypeNum", t)
            }

            static SaveChongWuTypeList(t) {
                var i = h.GetUserData("chongWuType");
                i[t] = 1, h.SetUserData("chongWuType", i)
            }

            static saveChongWuNum(t) {
                h.SetUserData("chongWuNum", t)
            }

            static AddExp(t) {
                var i = h.GetUserData("curExp"),
                    e = h.GetUserData("playerLv");
                (i += t) >= h.GetUserData("allExp") && (i = 0, e += 1, h.SetUserData("playerLv", e), Laya.stage.event("updateXianShi")), h.SetUserData("curExp", i)
            }

            static GetGuangKalv() {
                var t = h.GetUserData("showLv");
                return t > 6 && (t = D.RandomInt(1, 7)), t
            }
        }

        h.user = {}, h.userDV = {}, h.maxGuanQia = 100, h.maxPlayerLevel = 30, h.userDV.beijing = 1, h.userDV.yinxiao = 1, h.userDV.Gold = 0, h.userDV.Money = 0, h.userDV.showLv = 1, h.userDV.playerLv = 1, h.userDV.curExp = 0, h.userDV.allExp = 60, h.userDV.piFuType = {
            1: 1,
            2: 0,
            3: 0,
            4: 0,
            5: 0,
            6: 0
        }, h.userDV.piFuTypeNum = 1, h.userDV.chongWuType = {
            1: 0,
            2: 0,
            3: 0,
            4: 0,
            5: 0,
            6: 0
        }, h.userDV.chongWuNum = -1, h.userDV.isSign = 0, h.userDV.signNum = 0, h.userDV.canSignNum = 0;

        class l extends Laya.Script3D {
            constructor() {
                super()
            }

            onAwake() {
                Laya.timer.once(5e3, this, function () {
                    this.owner.destroy()
                })
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class u extends Laya.Script3D {
            constructor() {
                super()
            }

            onAwake() {
            }

            onUpdate() {
                var t = new Laya.Vector3(0, 1, 0),
                    i = new Laya.Quaternion;
                Laya.Quaternion.lookAt(D.mainCamera.transform.position, this.owner.transform.position, t, i), i.w = -i.w, this.owner.transform.rotation = i
            }

            onDisable() {
            }
        }

        class d extends Laya.Script3D {
            constructor() {
                super(), this.speed = .1, this.targetPos = null, this.initPos = new Laya.Vector3, this.rotateSpeed, this.hp = 10, this.anim, this.state = "waite", this.batPos, this.JingGao
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Idle"), this.JingGao = this.owner.getChildByName("JingGao"), this.JingGao.addComponent(u), this.JingGao.active = !1
            }

            init(t, i) {
                this.targetPos = i, this.batPos = t, this.state = "waiteInit"
            }

            hurt(t) {
                if (this.hp -= t, this.hp <= 0) {
                    var i = D.models.getChildByName("E9"),
                        e = Laya.Sprite3D.instantiate(i, D.curScene);
                    e.transform.position = this.owner.transform.position, e.addComponent(l), this.owner.active = !1
                }
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waiteInit":
                        if (null != this.batPos) {
                            var t = new Laya.Vector3(this.batPos.x, this.batPos.y, this.batPos.z),
                                i = new Laya.Vector3(this.batPos.x, this.owner.transform.position.y, this.batPos.z),
                                e = new Laya.Vector3(0, 1, 0),
                                a = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(i, this.owner.transform.position, e, a), a.w = -a.w;
                            var o = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, a, .1, o), this.owner.transform.rotation = o;
                            var n = new Laya.Vector3(0, 0, 0);
                            Laya.Vector3.subtract(this.owner.transform.position, t, n), Laya.Vector3.normalize(n, n), this.owner.transform.translate(new Laya.Vector3(-n.x * this.speed * Laya.timer.delta * .08, -n.y * this.speed * Laya.timer.delta * .08, -n.z * this.speed * Laya.timer.delta * .08), !1), Laya.Vector3.distance(this.owner.transform.position, t) < .5 && (this.speed = .2, this.JingGao.active = !0, this.anim.play("Attack"), this.state = "move")
                        }
                        break;
                    case "move":
                        null != this.targetPos && (t = new Laya.Vector3(this.targetPos.x, this.targetPos.y, this.targetPos.z), e = new Laya.Vector3(0, 1, 0), a = new Laya.Quaternion, Laya.Quaternion.lookAt(t, this.owner.transform.position, e, a), a.w = -a.w, o = new Laya.Quaternion, Laya.Quaternion.slerp(this.owner.transform.rotation, a, .1, o), this.owner.transform.rotation = o, n = new Laya.Vector3(0, 0, 0), Laya.Vector3.subtract(this.owner.transform.position, t, n), Laya.Vector3.normalize(n, n), this.owner.transform.translate(new Laya.Vector3(-n.x * this.speed * Laya.timer.delta * .08, -n.y * this.speed * Laya.timer.delta * .08, -n.z * this.speed * Laya.timer.delta * .08), !1), Laya.Vector3.distance(this.owner.transform.position, t) < .1 && (0 == D.carZhuang && (null != D.curPlayerControl && "win" != D.curPlayerControl.playerState && (D.curPlayerControl.stop(), null != D.cameraControl && D.cameraControl.toLose1(), null != D.curBoss && D.curBoss.toStop(), Laya.timer.scale = .5), D.carZhuang = !0), this.state = "stop"))
                }
            }

            onTriggerEnter(t) {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class m extends Laya.Script3D {
            constructor() {
                super(), this.anim
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator)
            }

            onUpdate() {
                var t = new Laya.Vector3(0, 1, 0),
                    i = new Laya.Quaternion;
                Laya.Quaternion.lookAt(D.mainCamera.transform.position, this.owner.transform.position, t, i), i.w = -i.w, this.owner.transform.rotation = i
            }

            setAnimSpeed(t) {
                this.anim.speed = t
            }

            onDisable() {
            }
        }

        class c extends Laya.Script3D {
            constructor() {
                super(), this.speed = .3, this.targetPos = null, this.initPos = new Laya.Vector3, this.rotateSpeed, this.hp = 10, this.Guangquan, this.state = "waite"
            }

            onAwake() {
                this.rotateSpeed = new Laya.Vector3(D.RandomFloat(-5, 5), D.RandomFloat(-5, 5), D.RandomFloat(-5, 5)), this.Guangquan = this.owner.getChildByName("Guangquan"), null != this.Guangquan && (this.Guangquan.addComponent(m), this.Guangquan.active = !1)
            }

            init(t) {
                this.targetPos = t
            }

            toMove() {
                this.state = "move"
            }

            hurt(t) {
                if (this.hp -= t, this.hp <= 0) {
                    if (-1 != this.owner.name.indexOf("Bomm")) {
                        D.PlaySound("BaoZha_Big");
                        var i = D.models.getChildByName("E5"),
                            e = Laya.Sprite3D.instantiate(i, D.curScene);
                        e.transform.position = this.owner.transform.position, e.transform.rotation = this.owner.transform.rotation, e.addComponent(l), null != D.curBoss && Laya.Vector3.distance(this.owner.transform.position, D.curBoss.owner.transform.position) < 100 && (r.ShowPreJiaYiUI(7e3, new Laya.Vector3(D.curBoss.owner.transform.position.x, this.owner.transform.position.y, D.curBoss.owner.transform.position.z), !0), D.curBoss.hurt(7e3)), Laya.timer.scale = .2, Laya.stage.event("timerHuiFu")
                    } else {
                        D.PlaySound("BaoZha_Small");
                        var a = D.models.getChildByName("E1"),
                            o = Laya.Sprite3D.instantiate(a, D.curScene);
                        o.transform.position = this.owner.transform.position, o.transform.rotation = this.owner.transform.rotation, o.addComponent(l)
                    }
                    this.owner.active = !1
                }
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale && "move" == this.state && null != this.targetPos) {
                    var t = new Laya.Vector3(this.targetPos.x, this.targetPos.y, this.targetPos.z),
                        i = new Laya.Vector3(0, 0, 0);
                    if (Laya.Vector3.subtract(this.owner.transform.position, t, i), Laya.Vector3.normalize(i, i), this.owner.transform.translate(new Laya.Vector3(-i.x * this.speed * Laya.timer.delta * .08, -i.y * this.speed * Laya.timer.delta * .08, -i.z * this.speed * Laya.timer.delta * .08), !1), this.owner.transform.rotate(this.rotateSpeed, !1, !1), 3 == h.GetUserData("showLv") && null != this.Guangquan && 1 == D.isJiaoXue && Laya.Vector3.distance(this.owner.transform.position, t) < 50) return this.Guangquan.active = !0, D.isGameStop = !0, this.stop(), D.cameraControl.toWaite(), null != D.curBoss && D.curBoss.stop(), null != r.gameUI && r.gameUI.showSheJiTiShi(this.Guangquan.transform.position), void (D.jiaXueType = "car");
                    Laya.Vector3.distance(this.owner.transform.position, t) < .5 && (0 == D.carZhuang && (null != D.curPlayerControl && "win" != D.curPlayerControl.playerState && (D.curPlayerControl.stop(), null != D.cameraControl && D.cameraControl.toLose1(), null != D.curBoss && D.curBoss.toStop(), Laya.timer.scale = .5), D.carZhuang = !0), this.owner.active = !1)
                }
            }

            stop() {
                this.state = "stop"
            }

            huiFu() {
                this.state = "move", 3 == h.GetUserData("showLv") && null != this.Guangquan && (this.Guangquan.active = !1, D.cameraControl.toWaiteInit(), null != r.gameUI && r.gameUI.hideSheJiTiShi())
            }

            onTriggerEnter(t) {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class y extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.HandSpawnPoint_L, this.HandSpawnPoint_M, this.HandSpawnPoint_R, this.state = "waite", this.hp = 27e3, this.allHp = 27e3, this.rengTimer = D.RandomInt(6, 12), this.bornTimer = D.RandomInt(10, 15), this.bornPos, this.Roar_FX, this.carList = [], this.Guangquan, this.XueTiaoXueTiao
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Idle"), this.HandSpawnPoint_L = D.FindChildByNameHelper(this.owner, "HandSpawnPoint_L"), this.bornPos = this.owner.getChildByName("bornPos"), this.Roar_FX = D.FindChildByNameHelper(this.owner, "Roar_FX"), this.Roar_FX.active = !1, this.Guangquan = D.FindChildByNameHelper(this.owner, "Guangquan"), null != this.Guangquan && (3 == h.GetUserData("showLv") && this.Guangquan.addComponent(m), this.Guangquan.active = !1), this.XueTiaoXueTiao = this.owner.getChildByName("XueTiaoXueTiao"), this.XueTiaoXueTiao.addComponent(u), this.XueTiaoXueTiao.active = !1
            }

            showGuangquan() {
                3 == h.GetUserData("showLv") && null != this.Guangquan && (this.Guangquan.active = !0, D.isGameStop = !0, this.stop(), D.cameraControl.toWaite(), null != r.gameUI && r.gameUI.showSheJiTiShi(this.Guangquan.transform.position), D.jiaXueType = "boss")
            }

            hurt(t) {
                "dead" != this.state && (this.hp -= t, this.hp <= 0 ? (D.PlaySound("Boss_Die"), this.hp = 0, this.state = "dead", Laya.timer.clearAll(this), this.Roar_FX.active = !0, D.cameraControl.toWaite(), D.curPlayerControl.win(), this.anim.crossFade("Dead", .1), D.jiShaNum += 1, null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1)) : t >= 7e3 && (this.anim.crossFade("GotHit", .1), Laya.timer.clearAll(this), Laya.timer.loop(5e3, this, function () {
                    D.PlaySound("Level1_4_Boss_Idle")
                }), Laya.timer.once(1e3, this, function () {
                    D.cameraControl.toMove(), this.anim.crossFade("LeftTurn", .1), this.state = "move"
                })), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.getChildByName("XueLiang").meshRenderer.material.tilingOffsetZ = .5 - this.hp / this.allHp * .5))
            }

            toStop() {
                this.anim.crossFade("Victory", .1), this.state = "stop", Laya.timer.clearAll(this)
            }

            paoXiao() {
                this.anim.crossFade("BattleCry", .1), D.PlaySound("Level1_4_Boss_Idle"), this.Roar_FX.active = !0, Laya.timer.once(2500, this, function () {
                    this.Roar_FX.active = !1
                }), Laya.timer.once(3500, this, function () {
                    this.anim.crossFade("BattleCry", .1), D.PlaySound("Level1_4_Boss_Idle"), this.Roar_FX.active = !0
                })
            }

            toMove() {
                this.anim.crossFade("LeftTurn", .1), this.state = "move", this.Roar_FX.active = !1, Laya.timer.loop(5e3, this, function () {
                    D.PlaySound("Level1_4_Boss_Idle")
                }), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !0), D.PlaySound("Level1_4_Boss_Run")
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waite":
                        break;
                    case "move":
                        if (null != D.cameraFocus) {
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(new Laya.Vector3(D.cameraFocus.transform.position.x, this.owner.transform.position.y, D.cameraFocus.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w;
                            var e = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, i, .02, e), this.owner.transform.rotation = e, this.reng(), this.born()
                        }
                }
            }

            born() {
                if (null != this.bornPos && (this.bornTimer -= .002 * Laya.timer.delta, this.bornTimer <= 0)) {
                    var t = D.RandomInt(0, this.bornPos.numChildren),
                        i = Laya.Sprite3D.instantiate(D.models.getChildByName("Bat"), this.owner);
                    i.transform.localPosition = this.bornPos.getChildAt(t).transform.localPosition, i.addComponent(d).init(this.bornPos.getChildAt(t).getChildAt(0).transform.position, D.cameraFocus.transform.position), this.bornTimer = D.RandomInt(10, 15)
                }
            }

            reng() {
                this.rengTimer -= .002 * Laya.timer.delta, this.rengTimer <= 0 && (this.anim.crossFade("AttackOneHand", .1), this.state = "waite", D.cameraControl.toWaite(), Laya.timer.once(1e3, this, function () {
                    var t = D.RandomInt(1, 4);
                    3 == h.GetUserData("showLv") && (t = 1);
                    var i = 0,
                        e = 0,
                        a = 0;
                    for (let l = 0; l < t; l++) {
                        var o, n = D.RandomInt(0, 11);
                        if (3 == h.GetUserData("showLv") && (n = 0), n > 7) o = D.models.getChildByName("Car_Bomm_" + D.RandomInt(1, 3));
                        else {
                            var s = D.RandomInt(1, 6);
                            3 == h.GetUserData("showLv") && (s = D.RandomInt(2, 5)), o = D.models.getChildByName("Car_" + s)
                        }
                        var r = Laya.Sprite3D.instantiate(o, this.HandSpawnPoint_L);
                        r.transform.localPosition = new Laya.Vector3(i, e, a), r.transform.localRotationEuler = new Laya.Vector3(D.RandomFloat(0, 360), D.RandomFloat(0, 360), D.RandomFloat(0, 360)), r.addComponent(c).init(D.cameraFocus.transform.position), this.carList.push(r), i = 0 == i ? -.1 : -.1 == i ? .1 : 0, e = .1, a = D.RandomFloat(-.1, .1)
                    }
                    Laya.timer.once(1500, this, function () {
                        for (let e = 0; e < this.carList.length; e++) {
                            var t = this.carList[e].transform.position.clone(),
                                i = this.carList[e].transform.getWorldLossyScale();
                            D.curScene.addChild(this.carList[e]), this.carList[e].transform.position = t, this.carList[e].transform.setWorldLossyScale(i), this.carList[e].getComponent(c).toMove()
                        }
                        this.carList.length = 0
                    })
                }), Laya.timer.once(6e3, this, function () {
                    "dead" != this.state && (D.cameraControl.toMove(), this.anim.crossFade("LeftTurn", .1), this.state = "move")
                }), this.rengTimer = D.RandomInt(6, 12))
            }

            stop() {
                Laya.timer.clearAll(this), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1), this.anim.speed = 0, this.state = "stop"
            }

            huiFu() {
                this.anim.speed = 1, null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !0), "dead" != this.state && (Laya.timer.once(3e3, this, function () {
                    this.anim.crossFade("LeftTurn", .1)
                }), this.state = "move", Laya.timer.loop(5e3, this, function () {
                    D.PlaySound("Level1_4_Boss_Idle")
                }), 3 == h.GetUserData("showLv") && null != this.Guangquan && (this.Guangquan.active = !1, D.cameraControl.toWaiteInit(), this.Roar_FX.active = !1, null != r.gameUI && r.gameUI.hideSheJiTiShi()))
            }

            QuaternionXiangJin(t, i) {
                var e = Math.abs(t.x) - Math.abs(i.x),
                    a = Math.abs(t.y) - Math.abs(i.y),
                    o = Math.abs(t.z) - Math.abs(i.z),
                    n = Math.abs(t.w) - Math.abs(i.w);
                return e < .01 && a < .01 && o < .01 && n < .01
            }

            getHpBi() {
                return this.hp / this.allHp
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class w extends Laya.Script3D {
            constructor() {
                super(), this.isZhuang = !1
            }

            onAwake() {
            }

            onUpdate() {
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    var i;
                    if (-1 != t.owner.name.indexOf("ShouShang") && 0 == this.isZhuang)
                        if (-1 != this.owner.name.indexOf("Funicular_barrel")) {
                            if (null != (i = this.owner.parent.parent.getComponent(g)) && 1 == i.isChuFa) {
                                this.isZhuang = !0;
                                var e = D.models.getChildByName("E9"),
                                    a = Laya.Sprite3D.instantiate(e, D.curScene);
                                a.transform.position = this.owner.transform.position, a.addComponent(l), null != D.curBoss && (r.ShowPreJiaYiUI(2e3, new Laya.Vector3(D.curBoss.owner.transform.position.x, this.owner.transform.position.y, D.curBoss.owner.transform.position.z), !0), D.curBoss.beiZhuang(2e3)), this.owner.active = !1
                            }
                        } else if (null != (i = this.owner.parent.getComponent(g)) && 1 == i.isChuFa && (i.poSui(), this.isZhuang = !0, null != D.curBoss)) {
                            var o = D.models.getChildByName("E21"),
                                n = Laya.Sprite3D.instantiate(o, D.curScene);
                            n.transform.position = new Laya.Vector3(D.curBoss.owner.transform.position.x, D.curBoss.owner.transform.position.y + 4, D.curBoss.owner.transform.position.z), n.addComponent(l), r.ShowPreJiaYiUI(6e3, new Laya.Vector3(D.curBoss.owner.transform.position.x, D.curBoss.owner.transform.position.y + 4, D.curBoss.owner.transform.position.z), !0), D.curBoss.beiZhuang(6e3)
                        }
                }
            }

            onDisable() {
            }
        }

        class g extends Laya.Script3D {
            constructor() {
                super(), this.type = "", this.animMove, this.sui, this.sui2, this.zheng, this.animSui, this.isChuFa = !1, this.Guangquan, this.JiGuanPian
            }

            onAwake() {
                if (this.type = this.owner.name, this.animMove = this.owner.getComponent(Laya.Animator), this.animMove.play("Idle"), this.Guangquan = this.owner.getChildByName("ButtonTrap").getChildByName("Button").getChildByName("Guangquan"), this.JiGuanPian = this.owner.getChildByName("ButtonTrap").getChildByName("Button").getChildByName("JiGuan"), null != this.Guangquan && this.Guangquan.addComponent(m), null != this.JiGuanPian && this.JiGuanPian.addComponent(u), -1 != this.type.indexOf("FunicularTrap")) this.owner.getChildByName("Funicular_Body").addComponent(w), this.sui = this.owner.getChildByName("Funicular_Body").getChildByName("Funicular_Parts"), this.sui2 = this.owner.getChildByName("Funicular_Body").getChildByName("Funicular_Parts"), this.zheng = this.owner.getChildByName("Funicular_Body").getChildByName("Funicular_mesh"), this.animSui = this.sui.getComponent(Laya.Animator), this.animSui.play("Idle"), this.sui.active = !1, this.sui2.active = !1;
                else if (-1 != this.type.indexOf("CraneTrap_Big")) this.owner.getChildByName("Crane_Body").addComponent(w), this.sui = this.owner.getChildByName("Crane_Body").getChildByName("Crane_Parts New"), this.sui2 = this.owner.getChildByName("Crane_Body").getChildByName("Crane_part_01"), this.zheng = this.owner.getChildByName("Crane_Body").getChildByName("Crane_UP"), this.animSui = this.sui.getComponent(Laya.Animator), this.animSui.play("Idle"), this.sui.active = !1, this.sui2.active = !1;
                else if (-1 != this.type.indexOf("Jiguan01")) {
                    var t = this.owner.getChildByName("Tong");
                    for (let i = 0; i < t.numChildren; i++) t.getChildAt(i).addComponent(w)
                }
            }

            showUI() {
                null != this.Guangquan && null != r.gameUI && r.gameUI.showSheJiTiShi(this.Guangquan.transform.position)
            }

            poSui() {
                if (-1 == this.type.indexOf("Jiguan01"))
                    if (this.animMove.speed = 0, this.zheng.active = !1, this.sui.active = !0, this.sui2.active = !0, -1 != this.type.indexOf("Right")) this.animSui.play("SuiR");
                    else if (-1 != this.type.indexOf("Left")) this.animSui.play("SuiL");
                    else {
                        var t = D.models.getChildByName("E9"),
                            i = Laya.Sprite3D.instantiate(t, D.curScene);
                        i.transform.position = this.sui.transform.position, i.addComponent(l), this.animSui.play("Sui")
                    }
            }

            toMove() {
                this.isChuFa = !0, -1 != this.type.indexOf("Jiguan01") ? this.animMove.play("Tong") : -1 != this.type.indexOf("Right") ? this.animMove.play("ChuFa_right") : this.animMove.play("ChuFa")
            }

            onUpdate() {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class p extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.bossPos, this.posIndex = 0, this.target = null, this.state = "waite", this.hp = 27e3, this.allHp = 27e3, this.speed = .1, this.isAttack = !1, this.attackTimer = D.RandomInt(20, 60), this.juLi = .5, this.Boss_Die_Pos, this.XueTiaoXueTiao, this.Guangquan
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Idle"), this.bossPos = D.curScene.getChildByName("bossPos"), this.Boss_Die_Pos = this.owner.getChildByName("Boss_Die_Pos"), this.XueTiaoXueTiao = this.owner.getChildByName("XueTiaoXueTiao"), this.XueTiaoXueTiao.addComponent(u), this.XueTiaoXueTiao.active = !1, this.Guangquan = D.FindChildByNameHelper(this.owner, "Guangquan"), null != this.Guangquan && (1 == h.GetUserData("showLv") && this.Guangquan.addComponent(m), this.Guangquan.active = !1)
            }

            showGuangquan() {
                1 == h.GetUserData("showLv") && null != this.Guangquan && (this.Guangquan.active = !0, D.isGameStop = !0, this.stop(), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1), null != r.gameUI && r.gameUI.showSheJiTiShi(this.Guangquan.transform.position), D.jiaXueType = "boss")
            }

            getNextTarget() {
                this.posIndex >= this.bossPos.numChildren && (this.posIndex = this.bossPos.numChildren - 1), this.target = this.bossPos.getChildAt(this.posIndex), this.posIndex += 1
            }

            beiZhuang(t) {
                "dead" != this.state && (this.anim.crossFade("Hit", .1), Laya.timer.once(500, this, function () {
                    this.anim.crossFade("Run", .1)
                }), this.hurt(t))
            }

            hurt(t) {
                "dead" != this.state && "win" != this.state && (this.hp -= t, this.hp <= 0 && (this.hp = 0, this.state = "dead", D.PlaySound("Boss_Die"), Laya.timer.clearAll(this), D.cameraControl.setShowTarget(this.Boss_Die_Pos, D.curGirl.Camera_Show_Player), D.curGirl.win(), this.anim.crossFade("Fall", .1), D.jiShaNum += 1, null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1)), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.getChildByName("XueLiang").meshRenderer.material.tilingOffsetZ = .5 - this.hp / this.allHp * .5))
            }

            toMove() {
                var t = D.curScene.getChildByName("kaiTouSui");
                if (null != t) {
                    for (let a = 0; a < t.numChildren; a++) {
                        t.getChildAt(a).getComponent(Laya.Animator).play("Sui");
                        var i = D.models.getChildByName("E8"),
                            e = Laya.Sprite3D.instantiate(i, D.curScene);
                        e.transform.position = t.getChildAt(a).getChildByName("FxPos").transform.position, e.addComponent(l)
                    }
                    D.PlaySound("JianZhuPoSui")
                }
                null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !0), this.getNextTarget(), this.anim.crossFade("Run", .1), this.state = "move", 1 == h.GetUserData("showLv") && null != this.Guangquan && Laya.timer.once(1e3, this, function () {
                    this.showGuangquan(), null != D.curGirl && D.curGirl.stop()
                })
            }

            attackStateChanage() {
                0 == this.isAttack && (this.attackTimer -= .3, this.attackTimer <= 0 && (D.RandomInt(0, 10) > 5 && (this.isAttack = !0, this.anim.crossFade("SweepDown_Left", .1), Laya.timer.once(1e3, this, function () {
                    this.anim.crossFade("Run", .1), this.isAttack = !1
                })), this.attackTimer = D.RandomInt(20, 60)))
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waite":
                        break;
                    case "move":
                        if (null != this.target) {
                            this.attackStateChanage();
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w;
                            var e = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, i, .015, e), this.owner.transform.rotation = e;
                            var a = new Laya.Vector3;
                            if (Laya.Vector3.subtract(this.owner.transform.position, this.target.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), this.posIndex >= this.bossPos.numChildren && null != D.curGirl && Laya.Vector3.distance(this.owner.transform.position, D.curGirl.owner.transform.position) < this.juLi) return Laya.timer.clearAll(this), this.state = "win", this.anim.speed = 1, this.anim.crossFade("SweepDown_Left", .1), Laya.timer.once(1e3, this, function () {
                                null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1), D.cameraControl.setShowTarget(this.Boss_Die_Pos, null), this.anim.crossFade("VictoryJump", .1), this.isAttack = !1
                            }), void D.curGirl.dead();
                            if (Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z)) < this.juLi && "dead" != this.state) {
                                if (this.posIndex >= this.bossPos.numChildren) return Laya.timer.clearAll(this), this.state = "win", this.anim.speed = 1, this.anim.crossFade("SweepDown_Left", .1), Laya.timer.once(1e3, this, function () {
                                    null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1), D.cameraControl.setShowTarget(this.Boss_Die_Pos, null), this.anim.crossFade("VictoryJump", .1), D.PlaySound("Level2_5_Boss_XiaoSheng"), this.isAttack = !1
                                }), void (null != D.curGirl && D.curGirl.dead());
                                1 == h.GetUserData("showLv") && 1 == this.posIndex && 1 == D.isJiaoXue && (D.isGameStop = !0, this.stop(), null != D.curGirl && D.curGirl.stop(), D.curScene.getChildByName("JiGuan").getChildAt(0).getComponent(g).showUI(), D.jiaXueType = "button"), this.getNextTarget(), this.posIndex == this.bossPos.numChildren - 1 && (this.speed = .15, this.anim.speed = 1.5, this.juLi = 2)
                            }
                        }
                }
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    t.owner.name.indexOf("Shadow_DestroyMode")
                }
            }

            stop() {
                this.anim.speed = 0, this.state = "stop"
            }

            huiFu() {
                null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !0), this.anim.speed = 1, this.state = "move", null != r.gameUI && r.gameUI.hideSheJiTiShi(), 1 == h.GetUserData("showLv") && null != this.Guangquan && (this.Guangquan.active = !1)
            }

            getHpBi() {
                return this.hp / this.allHp
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class f extends Laya.Script3D {
            constructor() {
                super(), this.state = "waite", this.chuMenPos, this.chuMenPos2, this.target, this.anim, this.speed = .04, this.JingGao, this.chiPos, this.type = "", this.hp = 10, this.allHp = 10, this.XueTiaoXueTiao, this.rigi, this.meshObj, this.Zombie_DieM
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Idle"), this.rigi = this.owner.getComponent(Laya.Rigidbody3D), this.rigi.isKinematic = !0, this.JingGao = this.owner.getChildByName("JingGao"), this.JingGao.addComponent(u), this.JingGao.active = !1, Laya.stage.on("ZombieStop", this, this.ZombieStop), Laya.stage.on("ZombieLuo", this, this.ZombieLuo), this.Zombie_DieM = D.models.getChildByName("Zombie_Die").meshRenderer.material, -1 != this.owner.name.indexOf("Big") ? (this.type = "Boss", this.allHp = 2e3, this.hp = this.allHp, this.XueTiaoXueTiao = this.owner.getChildByName("XueTiaoXueTiao"), this.XueTiaoXueTiao.addComponent(u), this.meshObj = D.FindChildByNameHelper(this.owner, "Zombie_Boss")) : (this.type = "Bing", this.allHp = 100, this.hp = this.allHp, this.meshObj = D.FindChildByNameHelper(this.owner, "Zombie Simple"))
            }

            init(t, i) {
                this.chuMenPos = t, this.chuMenPos2 = i, this.target = t, this.anim.play("Run"), this.state = "chuMen"
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waite":
                        break;
                    case "chuMen":
                        if (null != this.target) {
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w;
                            var e = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, i, .025, e), this.owner.transform.rotation = e;
                            var a = new Laya.Vector3;
                            Laya.Vector3.subtract(this.owner.transform.position, this.target.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z)) < .5 && (this.target == this.chuMenPos ? (this.target = this.chuMenPos2, null == this.target && (this.state = "move")) : this.state = "move")
                        }
                        break;
                    case "move":
                        null != D.curGirl && (t = new Laya.Vector3(0, 1, 0), i = new Laya.Quaternion, Laya.Quaternion.lookAt(new Laya.Vector3(D.curGirl.owner.transform.position.x, this.owner.transform.position.y, D.curGirl.owner.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w, e = new Laya.Quaternion, Laya.Quaternion.slerp(this.owner.transform.rotation, i, .025, e), this.owner.transform.rotation = e, a = new Laya.Vector3, Laya.Vector3.subtract(this.owner.transform.position, D.curGirl.owner.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(D.curGirl.owner.transform.position.x, this.owner.transform.position.y, D.curGirl.owner.transform.position.z)) < 8 ? 0 == this.JingGao.active && (this.JingGao.active = !0, 2 == h.GetUserData("showLv") && 1 == Laya.timer.scale && 1 == D.isJiaoXue && (Laya.timer.scale = .2)) : 1 == this.JingGao.active && (this.JingGao.active = !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(D.curGirl.owner.transform.position.x, this.owner.transform.position.y, D.curGirl.owner.transform.position.z)) < .5 && "jump" != D.curGirl.state && (D.curGirl.dead(), "Boss" == this.type ? (this.chiPos = D.curGirl.getChiPosBoss(), Laya.stage.event("ZombieStop"), this.state = "chi") : (this.chiPos = D.curGirl.getChiPos(), null == this.chiPos ? (Laya.stage.event("ZombieStop"), this.ZombieStop()) : this.state = "chi")));
                        break;
                    case "chi":
                        null != this.chiPos && (t = new Laya.Vector3(0, 1, 0), i = new Laya.Quaternion, Laya.Quaternion.lookAt(new Laya.Vector3(this.chiPos.transform.position.x, this.owner.transform.position.y, this.chiPos.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w, e = new Laya.Quaternion, Laya.Quaternion.slerp(this.owner.transform.rotation, i, .025, e), this.owner.transform.rotation = e, a = new Laya.Vector3, Laya.Vector3.subtract(this.owner.transform.position, this.chiPos.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(this.chiPos.transform.position.x, this.owner.transform.position.y, this.chiPos.transform.position.z)) < .1 && (this.owner.transform.rotation = this.chiPos.transform.rotation, this.anim.crossFade("Bitting_loop", .1), this.state = "kaiChi"));
                        break;
                    case "moveLuo":
                        a = new Laya.Vector3, this.owner.transform.getForward(a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed, a), this.owner.transform.translate(a, !1)
                }
            }

            ZombieLuo() {
                var t = new Laya.Vector3(0, 1, 0),
                    i = new Laya.Quaternion;
                Laya.Quaternion.lookAt(new Laya.Vector3(D.curGirl.owner.transform.position.x, this.owner.transform.position.y, D.curGirl.owner.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w, this.owner.transform.rotation = i, this.state = "moveLuo"
            }

            hurt(t) {
                "dead" != this.state && (this.hp -= t, -1 != this.owner.name.indexOf("Big") && D.PlaySound("Zombie_Hit"), this.hp <= 0 && (D.PlaySound("Zombie_Die"), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.active = !1), this.meshObj.skinnedMeshRenderer.material = this.Zombie_DieM, this.hp = 0, Laya.timer.clearAll(this), this.state = "dead", this.anim.crossFade("Dead", .1), D.jiShaNum += 1, 1 == this.JingGao.active && (this.JingGao.active = !1)), null != this.XueTiaoXueTiao && (this.XueTiaoXueTiao.getChildByName("XueLiang").meshRenderer.material.tilingOffsetZ = .5 - this.hp / this.allHp * .5))
            }

            baZhaHurt(t, i) {
                this.hurt(i), "dead" == this.state && (this.rigi.isTrigger = !1, this.rigi.isKinematic = !1, this.rigi.applyImpulse(new Laya.Vector3(5 * t.x, 4, 5 * t.z)), this.rigi.applyTorqueImpulse(new Laya.Vector3(D.RandomFloat(-5, 5), 0, D.RandomFloat(-5, 5))))
            }

            ZombieStop() {
                "chi" != this.state && "kaiChi" != this.state && "dead" != this.state && (this.state = "stop", this.anim.play("Idle"))
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    -1 != t.owner.name.indexOf("ZombieLuo") ? (this.state = "Luo", this.rigi.isKinematic = !1) : -1 != t.owner.name.indexOf("TrapBottom") && this.hurt(4e3)
                }
            }

            onDisable() {
                Laya.timer.clearAll(this), Laya.stage.off("ZombieStop", this, this.ZombieStop), Laya.stage.off("ZombieLuo", this, this.ZombieLuo)
            }
        }

        class L extends Laya.Script3D {
            constructor() {
                super(), this.npcList = [], this.damage = 1500
            }

            onAwake() {
            }

            onUpdate() {
            }

            baZha() {
                var t = D.models.getChildByName("E13"),
                    i = Laya.Sprite3D.instantiate(t, D.curScene);
                i.transform.position = this.owner.transform.position, i.addComponent(l), D.PlaySound("BaoZha_Small");
                for (let t = 0; t < this.npcList.length; t++) {
                    var e = this.npcList[t].getComponent(f);
                    if (null != e) {
                        var a = new Laya.Vector3;
                        Laya.Vector3.subtract(this.owner.transform.position, this.npcList[t].transform.position, a), Laya.Vector3.normalize(a, a), e.baZhaHurt(a, this.damage)
                    }
                }
                this.owner.active = !1
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    -1 != t.owner.name.indexOf("Zombie") && this.npcList.push(t.owner)
                }
            }

            onTriggerExit(t) {
                if (-1 != t.owner.name.indexOf("Zombie")) {
                    var i = this.npcList.indexOf(t.owner);
                    this.npcList.splice(i, 1)
                }
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class S extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.Shadow
            }

            onAwake() {
                this.Shadow = this.owner.getChildByName("Shadow"), this.anim = this.owner.getChildByName("TrapFromParts").getComponent(Laya.Animator), this.anim.play("Idle01")
            }

            luo() {
                this.anim.play("Luo"), D.PlaySound("BaoZha_Small"), Laya.timer.once(400, this, function () {
                    var t = D.models.getChildByName("E20"),
                        i = Laya.Sprite3D.instantiate(t, D.curScene);
                    i.transform.position = this.Shadow.transform.position, i.addComponent(l)
                }), Laya.timer.once(1e3, this, function () {
                    this.owner.active = !1
                })
            }

            onUpdate() {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class C extends Laya.Script3D {
            constructor() {
                super(), this.speed = 1, this.damage, this.targetPos = null, this.initPos = new Laya.Vector3
            }

            onAwake() {
                Laya.timer.once(6e3, this, function () {
                    this.owner.active = !1
                })
            }

            init(t, i) {
                this.damage = i, this.targetPos = t;
                var e = new Laya.Vector3(0, 1, 0),
                    a = new Laya.Quaternion;
                Laya.Quaternion.lookAt(this.targetPos, this.owner.transform.position, e, a), a.w = -a.w, this.owner.transform.rotation = a
            }

            onUpdate() {
                if (null != this.targetPos) {
                    var t = new Laya.Vector3(0, 0, 0);
                    this.owner.transform.getForward(t), Laya.Vector3.normalize(t, t), this.owner.transform.translate(new Laya.Vector3(-t.x * this.speed * Laya.timer.delta * .08, -t.y * this.speed * Laya.timer.delta * .08, -t.z * this.speed * Laya.timer.delta * .08), !1)
                }
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    if (-1 != t.owner.name.indexOf("Car")) {
                        var i = t.owner.getComponent(c);
                        return void (null != i && (3 == h.GetUserData("showLv") && "car" == D.jiaXueType && 1 == D.isGameStop && (null != D.curBoss && D.curBoss.huiFu(), i.huiFu(), D.isJiaoXue = !1, D.isGameStop = !1), i.hurt(this.damage), this.owner.active = !1))
                    }
                    if (-1 != t.owner.name.indexOf("ShouShang")) {
                        if (null != D.curBoss) return -1 != t.owner.name.indexOf("Head") ? (r.ShowPreJiaYiUI(3 * this.damage, this.targetPos, !0), D.curBoss.hurt(3 * this.damage)) : (r.ShowPreJiaYiUI(this.damage, this.targetPos, !1), D.curBoss.hurt(this.damage)), 3 == h.GetUserData("showLv") && "boss" == D.jiaXueType && 1 == D.isGameStop && (null != D.curBoss && D.curBoss.huiFu(), D.isGameStop = !1), 1 == h.GetUserData("showLv") && "boss" == D.jiaXueType && 1 == D.isGameStop && (null != D.curBoss && D.curBoss.huiFu(), null != D.curGirl && D.curGirl.huiFu(), D.isGameStop = !1), void (this.owner.active = !1)
                    } else {
                        if (-1 != t.owner.name.indexOf("Button")) {
                            var e = t.owner.parent.parent.getComponent(g);
                            if (null != e) {
                                if (1 == h.GetUserData("showLv"))
                                    if (1 == D.isGameStop) null != D.curBoss && D.curBoss.huiFu(), null != D.curGirl && D.curGirl.huiFu(), D.isJiaoXue = !1, D.isGameStop = !1;
                                    else if (1 == D.isJiaoXue) return void (this.owner.active = !1);
                                t.owner.active = !1, e.toMove(), this.owner.active = !1
                            }
                            return
                        }
                        if (-1 != t.owner.name.indexOf("Zombie")) {
                            var a;
                            if (-1 != t.owner.name.indexOf("Head")) {
                                if (null != (a = t.owner.parent.getComponent(f))) {
                                    r.ShowPreJiaYiUI(3 * this.damage, this.targetPos, !1);
                                    var o = D.models.getChildByName("E11");
                                    (n = Laya.Sprite3D.instantiate(o, D.curScene)).transform.position = this.owner.transform.position, n.addComponent(l), a.hurt(3 * this.damage), this.owner.active = !1
                                }
                            } else if (null != (a = t.owner.getComponent(f))) {
                                var n;
                                r.ShowPreJiaYiUI(this.damage, this.targetPos, !1), o = D.models.getChildByName("E11"), (n = Laya.Sprite3D.instantiate(o, D.curScene)).transform.position = this.owner.transform.position, n.addComponent(l), a.hurt(this.damage), this.owner.active = !1
                            }
                            return
                        }
                        if (-1 != t.owner.name.indexOf("YouTongChuFa")) {
                            var s = t.owner.parent.getComponent(L);
                            return void (null != s && (s.baZha(), this.owner.active = !1))
                        }
                        if (-1 != t.owner.name.indexOf("Bat")) {
                            var u = t.owner.getComponent(d);
                            return void (null != u && (u.hurt(this.damage), this.owner.active = !1))
                        }
                        if (-1 != t.owner.name.indexOf("BarrelTrapFrom")) {
                            var m = t.owner.parent.parent.getComponent(S);
                            if (null != m) {
                                t.owner.active = !1;
                                var y = D.models.getChildByName("E13"),
                                    w = Laya.Sprite3D.instantiate(y, D.curScene);
                                w.transform.position = t.owner.transform.position, w.addComponent(l), m.luo(), this.owner.active = !1
                            }
                            return
                        }
                    }
                }
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class v extends Laya.Script3D {
            constructor() {
                super(), this.curTouchId = 0, this.curTouchIdMove = 0, this.firstTouchMove = -1, this.lastMouseX = 0, this.lastMouseY = 0, this.rotaionSpeed = .05, this.isMouseDown = !1, this.playerState = "waite", this.speed = 1.5, this.normalSpeed = this.speed, this.speedMax = 1.5, this.dianTiSpeed = 2, this.maxX = 2.6, this.velocity = 6.7, this.t = .07, this.curPosX = 0, this.curPosY = 0, this.anim, this.initPos, this.initGravity, this.initFallSpeed, this.character, this.left = -.9, this.right = .9, this.rota, this.lastAngle = 180, this.rigi, this.body, this.rotaY = 0, this.animName = "Idle", this.shangcheng, this.firePos, this.damage = 5, this.Qiang, this.QiangType = "Duan", this.QiangCur, this.ziDanNum = 1
            }

            onAwake() {
                D.piFuType = h.GetUserData("piFuTypeNum"), this.Qiang = D.FindChildByNameHelper(this.owner, "Qiang"), this.body = this.owner.getChildAt(0), this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("idle"), this.updateShopYifu(D.piFuType - 1), D.PlaySound("ZhiShengJi", 0)
            }

            onEnable() {
                r.gameUI.bg.on(Laya.Event.MOUSE_DOWN, this, this.mouseDown), Laya.stage.on(Laya.Event.MOUSE_UP, this, this.mouseUp), Laya.stage.on(Laya.Event.MOUSE_OUT, this, this.mouseOut), Laya.stage.on("timerHuiFu", this, this.timerHuiFu)
            }

            updateShopYifu(t) {
                for (let i = 0; i < this.Qiang.numChildren; i++) this.Qiang.getChildAt(i).active = i == t;
                switch (this.QiangCur = this.Qiang.getChildAt(t), this.QiangType = t > 0 ? "Chang" : "Duan", this.firePos = this.QiangCur.getChildByName("ShootPoint"), this.firePos.active = !1, t) {
                    case 0:
                        this.damage = 100, this.ziDanNum = 1;
                        break;
                    case 1:
                        this.damage = 120, this.ziDanNum = 1;
                        break;
                    case 2:
                        this.damage = 120, this.ziDanNum = 2;
                        break;
                    case 3:
                        this.damage = 140, this.ziDanNum = 2;
                        break;
                    case 4:
                        this.damage = 110, this.ziDanNum = 3;
                        break;
                    case 5:
                        this.damage = 120, this.ziDanNum = 3
                }
            }

            onUpdate() {
                Laya.timer.delta > 300 || 0 != Laya.timer.scale && this.playerState
            }

            onLateUpdate() {
            }

            timerHuiFu() {
                Laya.timer.once(500, this, function () {
                    Laya.timer.scale = 1
                })
            }

            taiShou() {
            }

            mouseDown(t) {
                if (this.curTouchIdMove = t.touchId, this.curTouchId = t.touchId, 0 == this.isMouseDown) {
                    if ("waite" == this.playerState && (this.playerState = "showCameraInitWaite", null != r.gameUI && r.gameUI.unlockpiFuIndexList.length > 0)) {
                        r.pushUI = 1;
                        var i = D.RandomInt(0, r.gameUI.unlockpiFuIndexList.length);
                        return void r.ShowUIPanel("Push", !1, r.gameUI.unlockpiFuIndexList[i])
                    }
                    if ("showCameraInitWaite" == this.playerState && 0 == r.pushUI && (this.playerState = "showCameraInit"), "showCameraInit" == this.playerState && (this.playerState = "waitemove"), "waitemove" == this.playerState) return this.playerState = "stop", null != r.gameUI && r.gameUI.beginHide(), void D.cameraControl.begin();
                    "move" == this.playerState && (Laya.stage.on(Laya.Event.MOUSE_MOVE, this, this.Move), this.lastMouseX = Laya.stage.mouseX, this.lastMouseY = Laya.stage.mouseY, this.curPosX = 0, this.curPosY = 0, this.isMouseDown = !0, this.firstTouchMove = t.touchId, this.shoot())
                }
            }

            shoot() {
                2 == h.GetUserData("showLv") && Laya.timer.scale <= 1 && 1 == D.isJiaoXue && (Laya.timer.scale = 1, D.isJiaoXue = !1);
                var t = new Laya.Ray(new Laya.Vector3(0, 0, 0), new Laya.Vector3(0, 0, 0));
                D.mainCamera.viewportPointToRay(new Laya.Vector2(Laya.stage.mouseX * Laya.stage.clientScaleX, Laya.stage.mouseY * Laya.stage.clientScaleY), t);
                var i = [];
                if (D.curScene.physicsSimulation.rayCastAll(t, i), i.length > 0)
                    for (let t = 0; t < i.length; t++)
                        if (0 == D.isGameStop) {
                            if (1 == D.isJiaoXue) {
                                if ("Button" != i[t].collider.owner.name && "Barrel1" != i[t].collider.owner.name && "ZombieTrigger" != i[t].collider.owner.name && "Girl" != i[t].collider.owner.name && "ZombieLuo" != i[t].collider.owner.name) {
                                    this.faShe(i[t].point);
                                    break
                                }
                            } else if ("Barrel1" != i[t].collider.owner.name && "ZombieTrigger" != i[t].collider.owner.name && "Girl" != i[t].collider.owner.name && "ZombieLuo" != i[t].collider.owner.name) {
                                this.faShe(i[t].point);
                                break
                            }
                        } else if (1 == h.GetUserData("showLv")) {
                            if ("boss" == D.jiaXueType) {
                                if (-1 != i[t].collider.owner.name.indexOf("ShouShang")) {
                                    this.faShe(i[t].point);
                                    break
                                }
                            } else if ("button" == D.jiaXueType && "Button" == i[t].collider.owner.name) {
                                this.faShe(i[t].point);
                                break
                            }
                        } else if (3 == h.GetUserData("showLv"))
                            if ("boss" == D.jiaXueType) {
                                if (-1 != i[t].collider.owner.name.indexOf("ShouShang")) {
                                    this.faShe(i[t].point);
                                    break
                                }
                            } else if ("car" == D.jiaXueType && -1 != i[t].collider.owner.name.indexOf("Car")) {
                                this.faShe(i[t].point);
                                break
                            }
            }

            faShe(t) {
                var i = new Laya.Vector3(0, 1, 0),
                    e = new Laya.Quaternion;
                Laya.Quaternion.lookAt(t, this.body.transform.position, i, e), e.w = -e.w, this.body.transform.rotation = e, this.firePos.active = !1, this.firePos.active = !0, D.PlaySound("KaiQiang"), this.anim.crossFade("D_SheJi_" + this.QiangType, .1), D.cameraControl.CameraShake();
                var a = Laya.Sprite3D.instantiate(D.models.getChildByName("Bullet"), D.curScene);
                a.transform.position = this.firePos.transform.position, a.addComponent(C).init(t, this.damage);
                for (let i = 1; i < this.ziDanNum; i++) Laya.timer.once(200, this, function () {
                    this.firePos.active = !1, this.firePos.active = !0, D.PlaySound("KaiQiang"), this.anim.crossFade("D_SheJi_" + this.QiangType, .1), D.cameraControl.CameraShake();
                    var i = Laya.Sprite3D.instantiate(D.models.getChildByName("Bullet"), D.curScene);
                    i.transform.position = this.firePos.transform.position, i.addComponent(C).init(t, this.damage)
                })
            }

            ziDanShe() {
                this.curZiDannum -= 1, this.curZiDannum
            }

            Move(t) {
                if ("move" == this.playerState) {
                    if (t.touchId != this.curTouchId) return void (this.curTouchIdMove = t.touchId);
                    this.curTouchIdMove = t.touchId
                }
            }

            mouseUp(t) {
                t.touchId == this.curTouchId ? -1 != this.firstTouchMove ? (this.curTouchIdMove = this.firstTouchMove, this.curTouchId = this.firstTouchMove, t.touchId == this.firstTouchMove && (Laya.stage.off(Laya.Event.MOUSE_MOVE, this, this.Move), this.taiShou(), this.isMouseDown = !1, this.curTouchIdMove = 0, this.curPosY = 0, this.curPosX = 0)) : (Laya.stage.off(Laya.Event.MOUSE_MOVE, this, this.Move), this.taiShou(), this.isMouseDown = !1, this.curTouchIdMove = 0, this.curPosY = 0, this.curPosX = 0) : this.firstTouchMove = -1
            }

            mouseOut(t) {
                t.touchId == this.curTouchId ? -1 != this.firstTouchMove ? (this.curTouchIdMove = this.firstTouchMove, this.curTouchId = this.firstTouchMove, t.touchId == this.firstTouchMove && (Laya.stage.off(Laya.Event.MOUSE_MOVE, this, this.Move), this.taiShou(), this.isMouseDown = !1, this.curTouchIdMove = 0, this.curPosY = 0, this.curPosX = 0)) : (Laya.stage.off(Laya.Event.MOUSE_MOVE, this, this.Move), this.taiShou(), this.isMouseDown = !1, this.curTouchIdMove = 0, this.curPosY = 0, this.curPosX = 0) : this.firstTouchMove = -1
            }

            huiFu1() {
                null != D.curBoss && D.curBoss.toMove(), this.anim.crossFade("MiaoZhun_" + this.QiangType, .1), this.playerState = "move"
            }

            huiFu2() {
                null != D.curBoss && D.curBoss.toMove(), this.anim.crossFade("MiaoZhun_" + this.QiangType, .1), this.playerState = "move"
            }

            stop() {
                this.playerState = "stop"
            }

            lose() {
                this.playerState = "lose", Laya.timer.once(2e3, this, function () {
                    D.StopSound("ZhiShengJi"), r.ShowUIPanel("Fail")
                })
            }

            win() {
                this.playerState = "win", Laya.timer.once(2e3, this, function () {
                    D.StopSound("ZhiShengJi"), r.ShowUIPanel("Box")
                })
            }

            onTriggerStay(t) {
                1 != t.owner.destroyed && t.owner.name.indexOf("jieSuoTrigger")
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    t.owner.name.indexOf("Trampoline")
                }
            }

            onTriggerExit(t) {
                1 != t.owner.destroyed && t.owner.name.indexOf("zaBingTrigger")
            }

            Clamp(t, i, e) {
                return t < i && (t = i), t > e && (t = e), t
            }

            onDisable() {
                null != r.gameUI && r.gameUI.bg.off(Laya.Event.MOUSE_DOWN, this, this.mouseDown), Laya.stage.off(Laya.Event.MOUSE_UP, this, this.mouseUp), Laya.stage.off(Laya.Event.MOUSE_OUT, this, this.mouseOut), Laya.stage.off("timerHuiFu", this, this.timerHuiFu), Laya.timer.clearAll(this)
            }
        }

        class P extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.bossPos, this.posIndex = 0, this.target = null, this.state = "waite", this.hp = 100, this.allHp = 100, this.speed = .1, this.Camera_Show_Player
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Run"), this.bossPos = D.curScene.getChildByName("bossPos"), this.Camera_Show_Player = this.owner.getChildByName("Camera_Show_Player")
            }

            getNextTarget() {
                this.posIndex >= this.bossPos.numChildren && (this.posIndex = this.bossPos.numChildren - 1), this.target = this.bossPos.getChildAt(this.posIndex), this.posIndex += 1
            }

            hurt(t) {
                "dead" != this.state && (this.hp -= t, this.hp <= 0 && (Laya.timer.clearAll(this), this.state = "dead", D.cameraControl.toWaite(), D.curPlayerControl.win(), this.anim.crossFade("Shuaidao", .1)))
            }

            setSpeed(t) {
                this.speed = t
            }

            toMove() {
                this.getNextTarget(), this.state = "move"
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waite":
                        break;
                    case "move":
                        if (null != this.target) {
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w;
                            var e = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, i, .025, e), this.owner.transform.rotation = e;
                            var a = new Laya.Vector3;
                            Laya.Vector3.subtract(this.owner.transform.position, this.target.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z)) < .5 && (this.posIndex >= this.bossPos.numChildren ? this.dead() : (this.getNextTarget(), this.posIndex == this.bossPos.numChildren - 1 && (this.speed = .08, this.anim.speed = 1)))
                        }
                }
            }

            dead() {
                "dead" != this.state && (Laya.timer.clearAll(this), this.state = "dead", this.anim.crossFade("Shuaidao", .1))
            }

            win() {
                this.state = "win", this.anim.crossFade("Tiaowu", .1)
            }

            stop() {
                this.anim.speed = 0, this.state = "stop"
            }

            huiFu() {
                this.anim.speed = 1, this.state = "move"
            }

            getHpBi() {
                return this.hp / this.allHp
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class B extends Laya.Script3D {
            constructor() {
                super(), this.cameraState = "waiteInit", this.offect = new Laya.Vector3, this.anim, this.animZhenDong, this.speed = .05, this.initPos, this.initRotationEuler, this.MainCamera, this.MainCameraZ = 0, this.MainCameraY = 0, this.Camera, this.nextTarget = null, this.showTarget, this.showTwo, this.Plane, this.PlaneAnim
            }

            onAwake() {
                this.Camera = this.owner.getChildByName("Camera"), this.Plane = this.owner.getChildByName("Plane"), this.Plane.getChildByName("E3").active = !1, this.anim = this.owner.getChildByName("Camera").getComponent(Laya.Animator), this.anim.play("L1_01"), this.PlaneAnim = this.Plane.getComponent(Laya.Animator), this.PlaneAnim.play("Idle"), this.MainCamera = this.Camera.getChildByName("Camera1").getChildByName("Main Camera"), this.animZhenDong = this.Camera.getChildByName("Camera1").getComponent(Laya.Animator), this.animZhenDong.play("Idle1"), this.initRotationEuler = this.owner.transform.rotationEuler.clone()
            }

            CameraShake() {
                this.animZhenDong.play("Dou", 0, 0)
            }

            begin() {
                0 == D.guankaType ? (this.cameraState = "waite", this.owner.transform.rotationEuler = this.initRotationEuler, this.anim.play("L1_02"), null != D.curBoss && D.curBoss.paoXiao(), Laya.timer.once(3e3, this, function () {
                    this.anim.play("L1_03"), Laya.timer.once(1500, this, function () {
                        null != D.curPlayerControl && D.curPlayerControl.huiFu1(), this.cameraState = "move", null != D.curBoss && D.curBoss.showGuangquan()
                    })
                })) : 1 == D.guankaType ? (this.cameraState = "waite", this.owner.transform.rotationEuler = this.initRotationEuler, this.anim.play("L2_Idle"), this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("1").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("1").transform.rotation, this.owner.getChildByName("Plane").transform.position = this.owner.getChildByName("PlanePos2").transform.position, this.owner.getChildByName("Plane").transform.rotation = this.owner.getChildByName("PlanePos2").transform.rotation, null != D.curGirl && null != D.curBoss && (D.curGirl.toMove(), D.curGirl.setSpeed(D.curBoss.speed / 2)), this.cameraState = "lookAtGirl", Laya.timer.once(2e3, this, function () {
                    this.cameraState = "waite", this.anim.play("L2_02"), this.cameraState = "move", Laya.timer.once(2e3, this, function () {
                        null != D.curGirl && null != D.curBoss && D.curGirl.setSpeed(D.curBoss.speed), null != D.curPlayerControl && D.curPlayerControl.huiFu2()
                    })
                })) : 2 == D.guankaType && (this.cameraState = "waite", this.owner.transform.rotationEuler = this.initRotationEuler, 2 == D.guanKaLv ? (this.anim.play("L2_Idle"), this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("31").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("31").transform.rotation) : (this.anim.play("L2_Idle"), this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("61").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("61").transform.rotation), null != D.curGirl && D.curGirl.toMove(), this.cameraState = "lookAtGirlMove", Laya.timer.once(3e3, this, function () {
                    2 == D.guanKaLv ? (this.owner.getChildByName("Plane").transform.position = this.owner.getChildByName("PlanePos3").transform.position, this.owner.getChildByName("Plane").transform.rotation = this.owner.getChildByName("PlanePos3").transform.rotation, this.anim.play("L3_02")) : (this.owner.getChildByName("Plane").transform.position = this.owner.getChildByName("PlanePos6").transform.position, this.owner.getChildByName("Plane").transform.rotation = this.owner.getChildByName("PlanePos6").transform.rotation, this.anim.play("L6_02")), this.cameraState = "move", Laya.timer.once(2e3, this, function () {
                        null != D.curPlayerControl && D.curPlayerControl.huiFu2()
                    })
                }))
            }

            setShowTarget(t, i) {
                var e = this.owner.getChildByName("Camera").transform.position.clone(),
                    a = this.owner.getChildByName("Camera").transform.rotation.clone();
                this.anim.play("L2_Idle"), this.owner.getChildByName("Camera").transform.position = e, this.owner.getChildByName("Camera").transform.rotation = a, this.showTarget = t, this.showTwo = i, this.cameraState = "showTarget"
            }

            toMove() {
                this.cameraState = "move"
            }

            toWaite() {
                this.cameraState = "waite"
            }

            toWaiteInit() {
                this.cameraState = "waiteInit"
            }

            toLose1() {
                this.cameraState = "waite", this.anim.play("L1_04");
                var t = D.models.getChildByName("E2"),
                    i = Laya.Sprite3D.instantiate(t, D.curScene);
                i.transform.position = this.Plane.transform.position, i.transform.rotation = this.Plane.transform.rotation, i.addComponent(l), D.curPlayerControl.owner.active = !1, Laya.timer.once(1e3, this, function () {
                    Laya.timer.scale = 1, this.Plane.getChildByName("E3").active = !0, this.owner.transform.rotation = new Laya.Quaternion(0, 0, 0, 1), this.Plane.transform.position = this.owner.getChildByName("PlaneDead").transform.position, this.Plane.transform.rotation = this.owner.getChildByName("PlaneDead").transform.rotation, this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("CD").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("CD").transform.rotation, this.PlaneAnim.play("ZhuiLuo"), this.anim.play("ZhuiLuo", 0, 0), Laya.timer.once(1e3, this, function () {
                        D.PlaySound("BaoZha_Big"), D.curScene.getChildByName("BuildingpartsDead").getComponent(Laya.Animator).play("Sui"), D.PlaySound("JianZhuPoSui");
                        var t = D.models.getChildByName("E4_1"),
                            i = Laya.Sprite3D.instantiate(t, D.curScene);
                        i.transform.position = new Laya.Vector3(this.Plane.transform.position.x, this.Plane.transform.position.y + 5, this.Plane.transform.position.z), i.transform.rotation = this.Plane.transform.rotation, i.addComponent(l), null != D.curPlayerControl && D.curPlayerControl.lose()
                    })
                })
            }

            toOver() {
                this.cameraState = "waite", this.anim.play("L2_Idle"), this.owner.transform.position = D.curGirl.owner.transform.position.clone(), this.owner.transform.rotation = D.curGirl.owner.transform.rotation.clone(), this.Plane.transform.position = this.owner.getChildByName("Planepos").transform.position, this.Plane.transform.rotation = this.owner.getChildByName("Planepos").transform.rotation, this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("Over_1").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("Over_1").transform.rotation, Laya.timer.once(1e3, this, function () {
                    this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("Over_2").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("Over_2").transform.rotation
                }), Laya.timer.once(3e3, this, function () {
                    this.owner.getChildByName("Camera").transform.position = this.owner.getChildByName("Over_3").transform.position, this.owner.getChildByName("Camera").transform.rotation = this.owner.getChildByName("Over_3").transform.rotation, this.PlaneAnim.play("qiFei"), this.cameraState = "lookAtPlane", null != D.curPlayerControl && D.curPlayerControl.win()
                })
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }

            onLateUpdate() {
                switch (this.cameraState) {
                    case "waiteInit":
                        this.owner.transform.rotate(new Laya.Vector3(0, .1, 0), !1, !1);
                        break;
                    case "lookAtGirl":
                        if (null != D.curGirl) {
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(D.curGirl.owner.transform.position, this.owner.getChildByName("Camera").transform.position, t, i), i.w = -i.w, this.owner.getChildByName("Camera").transform.rotation = i
                        }
                        break;
                    case "lookAtGirlMove":
                        null != D.curGirl && (t = new Laya.Vector3(0, 1, 0), i = new Laya.Quaternion, Laya.Quaternion.lookAt(D.curGirl.owner.transform.position, this.owner.getChildByName("Camera").transform.position, t, i), i.w = -i.w, this.owner.getChildByName("Camera").transform.rotation = i, null != D.curGirl && (this.owner.transform.position = D.curGirl.owner.transform.position));
                        break;
                    case "lookAtPlane":
                        null != this.Plane && (t = new Laya.Vector3(0, 1, 0), i = new Laya.Quaternion, Laya.Quaternion.lookAt(this.Plane.transform.position, this.owner.getChildByName("Camera").transform.position, t, i), i.w = -i.w, this.owner.getChildByName("Camera").transform.rotation = i);
                        break;
                    case "move":
                        if (0 == D.guankaType) this.owner.transform.rotate(new Laya.Vector3(0, .1, 0), !1, !1);
                        else if (1 == D.guankaType) {
                            if (null != D.curGirl && null != D.curBoss) {
                                var e = new Laya.Vector3;
                                if (Laya.Vector3.subtract(D.curGirl.owner.transform.position, D.curBoss.owner.transform.position, e), e = new Laya.Vector3(e.x / 2, e.y / 2, e.z / 2), Laya.Vector3.add(D.curBoss.owner.transform.position, e, e), this.owner.transform.position = e, null != D.curBoss.target) {
                                    var a = new Laya.Quaternion;
                                    Laya.Quaternion.slerp(this.owner.transform.rotation, D.curBoss.target.transform.rotation, .01, a), this.owner.transform.rotation = a
                                }
                            }
                        } else 2 == D.guankaType && null != D.curGirl && (2 == D.guanKaLv ? this.owner.transform.position = D.curGirl.owner.transform.position : this.owner.transform.position = D.curGirl.CameraPos.transform.position, null != D.curGirl.target) && (a = new Laya.Quaternion, Laya.Quaternion.slerp(this.owner.transform.rotation, D.curGirl.target.transform.rotation, .01, a), this.owner.transform.rotation = a);
                        break;
                    case "showTarget":
                        if (null != this.showTarget) {
                            a = new Laya.Quaternion, Laya.Quaternion.slerp(this.Camera.transform.rotation, this.showTarget.transform.rotation, .05, a), this.Camera.transform.rotation = a;
                            var o = new Laya.Vector3;
                            Laya.Vector3.lerp(this.Camera.transform.position, this.showTarget.transform.position, .05, o), this.Camera.transform.position = o, Laya.Vector3.distance(this.Camera.transform.position, this.showTarget.transform.position) < .1 && (this.cameraState = "waiteShow", null != this.showTwo ? Laya.timer.once(500, this, function () {
                                this.showTarget = this.showTwo, this.showTwo = null, this.cameraState = "showTarget"
                            }) : 1 == D.guankaType ? -1 != this.showTarget.name.indexOf("Boss") ? null != D.curPlayerControl && D.curPlayerControl.lose() : null != D.curPlayerControl && D.curPlayerControl.win() : 2 == D.guankaType && null != D.curPlayerControl && D.curPlayerControl.lose())
                        }
                }
            }
        }

        class b extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.Destroy, this.Full, this.FangDing, this.type = 1
            }

            onAwake() {
                if (-1 != this.owner.name.indexOf("Fang")) this.type = 2, this.anim = this.owner.getChildByName("Fang").getComponent(Laya.Animator), this.anim.play("Idle");
                else {
                    this.type = 1, this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Idle"), this.Destroy = this.owner.getChildByName("Destroy"), this.Full = this.owner.getChildByName("Full"), this.FangDing = this.owner.getChildByName("FangDing"), this.Destroy.active = !1;
                    var t = D.RandomInt(0, this.FangDing.numChildren);
                    for (let i = 0; i < this.FangDing.numChildren; i++) this.FangDing.getChildAt(i).active = i == t
                }
            }

            poSui() {
                1 == this.type && (this.Full.active = !1, this.Destroy.active = !0), D.PlaySound("JianZhuPoSui"), this.anim.play("Sui")
            }

            onUpdate() {
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    -1 != t.owner.name.indexOf("ShouShang") ? 1 == this.type ? 1 == this.Full.active && this.poSui() : this.poSui() : -1 != t.owner.name.indexOf("Car") && (1 == this.type ? 1 == this.Full.active && this.poSui() : this.poSui())
                }
            }

            onDisable() {
            }
        }

        class x extends Laya.Script3D {
            constructor() {
                super(), this.ZombiePos, this.doorAnim, this.chuMenPos, this.chuMenPos2, this.bornNum = 5, this.ZombiePre
            }

            onAwake() {
                -1 == this.owner.name.indexOf("NoAnim") && (this.doorAnim = this.owner.getComponent(Laya.Animator), this.doorAnim.play("Idle")), this.ZombiePos = this.owner.getChildByName("ZombiePos"), this.chuMenPos = this.owner.getChildByName("chuMenPos"), this.ZombiePre = D.models.getChildByName("Zombie")
            }

            init(t) {
                this.chuMenPos2 = D.curScene.getChildByName("ZombiePos").getChildAt(t)
            }

            beginBorn() {
                null != this.doorAnim && (this.doorAnim.play("Open"), D.PlaySound("PoMen")), Laya.timer.loop(500, this, this.bornZombie)
            }

            bornBoss(t, i) {
                var e = Laya.Sprite3D.instantiate(D.models.getChildByName("ZombieBig"), D.curScene);
                e.transform.position = t.transform.position, e.transform.rotation = t.transform.rotation, e.addComponent(f).init(i, null)
            }

            bornZombie() {
                this.bornNum -= 1;
                var t = Laya.Sprite3D.instantiate(this.ZombiePre, D.curScene);
                t.transform.position = this.ZombiePos.transform.position, t.transform.rotation = this.ZombiePos.transform.rotation, t.addComponent(f).init(this.chuMenPos, this.chuMenPos2), this.bornNum <= 0 && Laya.timer.clear(this, this.bornZombie)
            }

            onUpdate() {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class T extends Laya.Script3D {
            constructor() {
                super(), this.anim, this.bossPos, this.posIndex = 0, this.target = null, this.state = "waite", this.hp = 100, this.allHp = 100, this.speed = .03, this.Camera_Show_Player, this.chiPos, this.chiNum = -1, this.CameraPos
            }

            onAwake() {
                this.anim = this.owner.getComponent(Laya.Animator), this.anim.play("Run"), this.bossPos = D.curScene.getChildByName("bossPos"), this.Camera_Show_Player = this.owner.getChildByName("Camera_Show_Player"), this.CameraPos = this.owner.getChildByName("CameraPos"), this.chiPos = this.owner.getChildByName("chiPos")
            }

            getNextTarget() {
                this.posIndex >= this.bossPos.numChildren && (this.posIndex = this.bossPos.numChildren - 1), this.target = this.bossPos.getChildAt(this.posIndex), this.posIndex += 1
            }

            hurt(t) {
                "dead" != this.state && (this.hp -= t, this.hp <= 0 && (Laya.timer.clearAll(this), this.state = "dead", D.cameraControl.toWaite(), D.curPlayerControl.win(), this.anim.crossFade("Shuaidao", .1)))
            }

            setSpeed(t) {
                this.speed = t
            }

            toMove() {
                this.getNextTarget(), this.state = "move"
            }

            getChiPosBoss() {
                return 1 == this.chiNum ? this.chiPos.getChildAt(2) : this.chiPos.getChildAt(1)
            }

            getChiPos() {
                return this.chiNum += 1, this.chiNum > 2 ? null : this.chiPos.getChildAt(this.chiNum)
            }

            onUpdate() {
                if (!(Laya.timer.delta > 300) && 0 != Laya.timer.scale) switch (this.state) {
                    case "waite":
                        break;
                    case "move":
                        if (null != this.target) {
                            var t = new Laya.Vector3(0, 1, 0),
                                i = new Laya.Quaternion;
                            Laya.Quaternion.lookAt(new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z), this.owner.transform.position, t, i), i.w = -i.w;
                            var e = new Laya.Quaternion;
                            Laya.Quaternion.slerp(this.owner.transform.rotation, i, .025, e), this.owner.transform.rotation = e;
                            var a = new Laya.Vector3;
                            if (Laya.Vector3.subtract(this.owner.transform.position, this.target.transform.position, a), Laya.Vector3.normalize(a, a), Laya.Vector3.scale(a, -this.speed * Laya.timer.delta * .08, a), this.owner.transform.translate(a, !1), Laya.Vector3.distance(this.owner.transform.position, new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z)) < .1)
                                if (this.posIndex >= this.bossPos.numChildren) {
                                    this.owner.transform.position = new Laya.Vector3(this.target.transform.position.x, this.owner.transform.position.y, this.target.transform.position.z), this.owner.transform.rotation = this.target.transform.rotation, D.cameraControl.toOver();
                                    var o = this.owner.transform.position.clone(),
                                        n = this.owner.transform.rotation.clone();
                                    D.cameraControl.Plane.addChild(this.owner), this.owner.transform.position = o, this.owner.transform.rotation = n, this.anim.play("TiaoFeiJi"), Laya.stage.event("ZombieLuo"), this.state = "jump"
                                } else this.getNextTarget(), this.posIndex, this.bossPos.numChildren
                        }
                }
            }

            jump() {
            }

            dead() {
                "dead" != this.state && (D.cameraControl.setShowTarget(this.Camera_Show_Player, null), Laya.timer.clearAll(this), this.state = "dead", this.anim.crossFade("Shuaidao", .1))
            }

            win() {
                this.state = "win", this.anim.crossFade("Tiaowu", .1)
            }

            stop() {
                this.anim.speed = 0, this.state = "stop"
            }

            huiFu() {
                this.anim.speed = 1, this.state = "move"
            }

            onTriggerEnter(t) {
                if (t) {
                    if (null == t.owner) return;
                    if (1 == t.owner.destroyed) return;
                    if (-1 != t.owner.name.indexOf("BornTrigger")) {
                        t.owner.active = !1;
                        var i = t.owner.getChildByName("bossPos"),
                            e = D.curScene.getChildByName("ZombiePos").getChildIndex(t.owner),
                            a = D.curScene.getChildByName("Fang").getChildAt(e).getComponent(x);
                        a.beginBorn(), null != i && a.bornBoss(i, t.owner)
                    }
                }
            }

            getHpBi() {
                return this.hp / this.allHp
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }
        }

        class N extends Laya.Script3D {
            constructor() {
                super()
            }

            onEnable() {
            }

            onDisable() {
                Laya.timer.clearAll(this)
            }

            onUpdate() {
            }

            CreatePlayer() {
                D.beiShu = 0, D.currentPiFuType = -1, D.guankaType = D.guanKaLv % 3, D.curBoss = null, D.curGirl = null, D.jiShaNum = 0, D.carZhuang = !1, D.isGameStop = !1, h.GetUserData("showLv") <= 3 ? D.isJiaoXue = !0 : D.isJiaoXue = !1;
                var t = D.curScene.getChildByName("Camera").getChildByName("Plane").getChildByName("Player");
                if (D.curPlayerControl = t.addComponent(v), 0 == D.guankaType) {
                    D.curBoss = D.curScene.getChildByName("Boss_1").addComponent(y);
                    var i = D.curScene.getChildByName("Buildingparts");
                    if (null != i)
                        for (let t = 0; t < i.numChildren; t++) i.getChildAt(t).addComponent(b)
                } else if (1 == D.guankaType) {
                    D.curBoss = D.curScene.getChildByName("Boss_2").addComponent(p), D.curGirl = D.curScene.getChildByName("Girl").addComponent(P);
                    var e = D.curScene.getChildByName("JiGuan");
                    if (null != e)
                        for (let t = 0; t < e.numChildren; t++) e.getChildAt(t).addComponent(g);
                    var a = D.curScene.getChildByName("ZhuangSui");
                    if (null != a)
                        for (let t = 0; t < a.numChildren; t++) a.getChildAt(t).addComponent(b)
                } else if (2 == D.guankaType) {
                    D.curGirl = D.curScene.getChildByName("Girl").addComponent(T);
                    var o = D.curScene.getChildByName("Fang");
                    if (null != o)
                        for (let t = 0; t < o.numChildren; t++) o.getChildAt(t).addComponent(x).init(t);
                    var n = D.curScene.getChildByName("BaoZha");
                    if (null != n)
                        for (let t = 0; t < n.numChildren; t++) n.getChildAt(t).addComponent(L);
                    var s = D.curScene.getChildByName("TrapFrom");
                    if (null != s)
                        for (let t = 0; t < s.numChildren; t++) s.getChildAt(t).addComponent(S)
                }
                D.cameraControl = D.curScene.getChildByName("Camera").addComponent(B)
            }

            initLv() {
            }
        }

        class D {
            static PlaySound(t, i = 1) {
                if (0 != h.GetUserData("yinxiao")) {
                    var e = "res/audio/" + t;
                    return Laya.SoundManager.playSound(e + ".mp3", i, null)
                }
            }

            static PlaySoundUpdate(t) {
                if (0 != h.GetUserData("yinxiao") && 0 == D.isSound) {
                    D.isSound = !0;
                    var i = "res/audio/" + t;
                    Laya.SoundManager.playSound(i + ".mp3", 1, Laya.Handler.create(this, function () {
                        D.isSound = !1
                    }))
                }
            }

            static StopSound(t) {
                var i = "res/audio/" + t;
                Laya.SoundManager.stopSound(i + ".mp3")
            }

            static PlayMusic(t, i = 0) {
                if (D.preMusicName != t && 0 != h.GetUserData("beijing")) {
                    D.preMusicName = t, D.bjMusic && (D.bjMusic.stop(), D.bjMusic = null);
                    var e, a = "res/audio/" + t;
                    return e = Laya.SoundManager.playMusic(a + ".mp3", i), D.bjMusic = e, e
                }
            }

            static StopMusic() {
                D.bjMusic && (D.bjMusic.stop(), D.bjMusic = null), D.preMusicName = ""
            }

            static SetMusicVolume(t) {
                D.bjMusic && (D.bjMusic.volume = t)
            }

            static PlayVibrate() {
                window.wx ? wx.vibrateShort() : window.swan ? swan.vibrateShort() : window.navigator && window.navigator.vibrate && window.navigator.vibrate(20)
            }

            static RandomInt(t, i) {
                return Math.floor(Math.random() * (i - t) + t)
            }

            static RandomFloat(t, i) {
                return Math.random() * (i - t) + t
            }

            static toTwoTimeFormat(t) {
                var i = Math.floor(t % 3600 / 60),
                    e = Math.floor(t % 3600 % 60);
                return i < 10 && (i = "0" + i), e < 10 && (e = "0" + e), i + ":" + e
            }

            static TotimeFormat(t) {
                var i = Math.floor(t / 3600),
                    e = Math.floor(t % 3600 / 60),
                    a = Math.floor(t % 3600 % 60);
                return i < 10 && (i = "0" + i), e < 10 && (e = "0" + e), a < 10 && (a = "0" + a), i + ":" + e + ":" + a
            }

            static getWeekOfYear() {
                var t = new Date,
                    i = new Date(t.getFullYear(), 0, 1),
                    e = i.getDay(),
                    a = 1;
                0 != e && (a = 7 - e + 1), i = new Date(t.getFullYear(), 0, 1 + a);
                var o = Math.ceil((t.valueOf() - i.valueOf()) / 864e5);
                return Math.ceil(o / 7) + 1
            }

            static FindChild(t, i) {
                for (var e = [], a = 0; a < t.length; a++) {
                    var o = t[a];
                    if (o.name == i) return o;
                    o.numChildren && (e = e.concat(o._children))
                }
                return e.length ? D.FindChild(e, i) : null
            }

            static FindChildByNameHelper(t, i) {
                if (t.name == i) return t;
                var e = t.numChildren,
                    a = null;
                for (let o = 0; o < e && !(a = D.FindChildByNameHelper(t.getChildAt(o), i)); ++o) ;
                return a
            }

            static GetCirclePoint(t) {
                var i = D.RandomFloat(0, 2 * Math.PI),
                    e = 2 * Math.cos(i),
                    a = 2 * Math.sin(i),
                    o = new Laya.Vector3(e, 0, a);
                return Laya.Vector3.add(new Laya.Vector3(t.x, t.y, t.z), o, o), o
            }

            static AngleBetweenVector(t, i) {
                var e = Laya.Vector3.dot(t, i) / (Laya.Vector3.scalarLength(t) * Laya.Vector3.scalarLength(i));
                return 180 * Math.acos(e) / Math.PI
            }

            static NFormatter(t) {
                const i = [{
                    value: 1,
                    symbol: ""
                }, {
                    value: 1e3,
                    symbol: "k"
                }, {
                    value: 1e6,
                    symbol: "m"
                }, {
                    value: 1e9,
                    symbol: "g"
                }, {
                    value: 1e12,
                    symbol: "t"
                }, {
                    value: 1e15,
                    symbol: "p"
                }, {
                    value: 1e18,
                    symbol: "e"
                }];
                let e;
                for (e = i.length - 1; e > 0 && !(t >= i[e].value); e--) ;
                return (t / i[e].value).toFixed(0).replace(/\.0+$|(\.[0-9]*[1-9])0+$/, "$1") + i[e].symbol
            }

            static ShowMoney3D(t, i) {
                for (var e = D.NFormatter(t).split(""), a = .16 * (e.length - 1) * .5, o = 1; o <= 5; o++)
                    if (o <= e.length) {
                        i.getChildAt(o - 1).active = !0, i.getChildAt(o - 1).transform.localPositionX = .16 * -(o - 1) + a, i.getChildAt(o - 1).transform.localPositionZ = -.3;
                        for (var n = 0; n < i.getChildAt(o - 1).numChildren; n++) e[o - 1] == i.getChildAt(o - 1).getChildAt(n).name ? i.getChildAt(o - 1).getChildAt(n).active = !0 : i.getChildAt(o - 1).getChildAt(n).active = !1
                    } else i.getChildAt(o - 1).active = !1
            }

            static updateShuZi3D(t, i, e) {
                for (var a = t.toString().split(""), o = -(a.length - 1) * e * .5, n = 0; n < i.numChildren; n++)
                    if (n <= a.length) {
                        i.getChildAt(n).active = !0, i.getChildAt(n).transform.localPositionX = n * e + o;
                        for (var s = 0; s < i.getChildAt(n).numChildren; s++) a[n] == i.getChildAt(n).getChildAt(s).name ? i.getChildAt(n).getChildAt(s).active = !0 : i.getChildAt(n).getChildAt(s).active = !1
                    } else i.getChildAt(n).active = !1
            }

            static GetDirForce(t, i, e) {
                var a = t,
                    o = i,
                    n = new Laya.Vector3((o.x - a.x) / 3, (o.y - a.y) / 3 + 2.1, (o.z - a.z) / 3),
                    s = new Laya.Vector3;
                return Laya.Vector3.scale(n, e, s), s
            }

            static loadScene(t, i) {
                null != D.curScene && (D.curScene.destroy(), D.curScene = null), Laya.loader.create(t, Laya.Handler.create(this, function () {
                    if (D.curScene = Laya.loader.getRes(t), D.curScene) {
                        if (Laya.stage.addChild(D.curScene), D.curScene.zOrder = -1, D.mainCamera = D.curScene.getChildByName("Camera").getChildByName("Camera").getChildByName("Camera1").getChildByName("Main Camera"), D.curLevelManager = D.curScene.addComponent(N), D.cameraTrans = D.curScene.getChildByName("Camera"), D.cameraFocus = D.curScene.getChildByName("Camera").getChildByName("Camera"), SdkUtil.GetConfig && 0 == SdkUtil.GetConfig("openlight")) {
                            var e = D.curScene.getChildByName("Directional Light");
                            e.shadowMode = Laya.ShadowMode.Hard, e.shadowStrength = .5, e.shadowDistance = 80, e.shadowResolution = 2048
                        }
                        i && i()
                    } else D.loadScene(t, i)
                }))
            }
        }

        D.curScene = null, D.curLevelManager = null, D.curPlayerControl = null, D.models = null, D.mainCamera = null, D.cameraFocus = null, D.cameraTrans = null, D.cameraControl = null, D.Config = {}, D.guanKaLv = 1, D.piFuType = 1, D.currentPiFuType = -1, D.beiShu = 0, D.curBoss = null, D.curGirl = null, D.isSound = !1, D.isGameStop = !1, D.isJiaoXue = !1, D.guankaType = 1, D.carZhuang = !1, D.jiShaNum = 0, D.jiaXueType = "boss";

        class U extends Laya.Scene {
            constructor() {
                super(), this.xiangZiNum = 0, this.jinBiList = new Array, this.xiangZiRandom = 3, this.xiangZiAllNum = 0
            }

            onEnable() {
                100 == SdkUtil.GetConfig("box") && (this.xiangZiRandom = D.RandomInt(1, 4)), window.SdkUtil.ShowBanner && window.SdkUtil.ShowBanner(), null != this.ADPanel && SdkUtil.ShowNeiZhiAD && SdkUtil.ShowNeiZhiAD(this.ADPanel, 3), Laya.SoundManager.stopAllSound();
                for (let i = 1; i <= 9; i++) {
                    var t = 30 * i;
                    this.jinBiList.push(t)
                }
                for (let t = 1; t <= 9; t++) {
                    var i = D.RandomInt(0, this.jinBiList.length);
                    this["num" + t].text = this.jinBiList[i], this.jinBiList.splice(i, 1), this["qian" + t].visible = !1
                }
                this.fangQi.visible = !1, this.zaiLai.visible = !1, this.updateUI(), this.xiangZi1.on(Laya.Event.CLICK, this, function () {
                    this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi1.visible = !1, this.qian1.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num1.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZiAllNum += 1, this.xiangZi1.visible = !1, this.qian1.visible = !0, h.AddProp(1, 1 * this.num1.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi2.on(Laya.Event.CLICK, this, function () {
                    this.xiangZiNum += 1, D.PlaySound("Btn"), this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi2.visible = !1, this.qian2.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num2.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi2.visible = !1, this.qian2.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num2.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi3.on(Laya.Event.CLICK, this, function () {
                    this.xiangZiNum += 1, D.PlaySound("Btn"), this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi3.visible = !1, this.qian3.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num3.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi3.visible = !1, this.qian3.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num3.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi4.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi4.visible = !1, this.qian4.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num4.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi4.visible = !1, this.qian4.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num4.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi5.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi5.visible = !1, this.qian5.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num5.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi5.visible = !1, this.qian5.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num5.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi6.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi6.visible = !1, this.qian6.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num6.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi6.visible = !1, this.qian6.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num6.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi7.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi7.visible = !1, this.qian7.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num7.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi7.visible = !1, this.qian7.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num7.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi8.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi8.visible = !1, this.qian8.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num8.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi8.visible = !1, this.qian8.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num8.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.xiangZi9.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.xiangZiNum += 1, this.xiangZiNum > this.xiangZiRandom ? window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZi9.visible = !1, this.qian9.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num9.text), r.ShowGameTipUI("You claimed!", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this))) : (this.xiangZi9.visible = !1, this.qian9.visible = !0, this.xiangZiAllNum += 1, h.AddProp(1, 1 * this.num9.text), r.ShowGameTipUI("You claimed!", 300)), this.updateUI()
                }), this.zaiLai.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("宝箱页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (this.xiangZiNum = 0, this.xiangZiRandom = 3, this.fangQi.visible = !1, this.zaiLai.visible = !1, this.updateUI(), r.ShowGameTipUI("You got keys", 300), SdkUtil.TDEvent("宝箱页面视频完成"))
                    }.bind(this)))
                }), this.fangQi.on(Laya.Event.CLICK, this, function () {
                    this.destroy(), r.ShowUIPanel("Win")
                })
            }

            updateUI() {
                if (this.xiangZiNum >= this.xiangZiRandom) {
                    for (let t = 1; t <= this.allBtn.numChildren; t++) this["ad" + t].alpha = 1;
                    this.fangQi.visible = !0, this.zaiLai.visible = !0
                } else
                    for (let t = 1; t <= this.allBtn.numChildren; t++) this["ad" + t].alpha = 0;
                this.xiangZiAllNum >= 9 && (this.fangQi.visible = !0, this.zaiLai.visible = !1)
            }

            onDisable() {
                Laya.timer.clearAll(this), window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner()
            }
        }

        class k extends Laya.Scene {
            constructor() {
                super()
            }

            onEnable() {
                this.fangQi.on(Laya.Event.CLICK, this, function (t) {
                    D.PlaySound("Btn"), this.destroy()
                }), this.lingQu.on(Laya.Event.CLICK, this, function (t) {
                    D.PlaySound("Btn"), SdkUtil.TDEvent("视频点击推送加钱"), window.SdkUtil.ShowVideo(function (t) {
                        if (1 == t) {
                            var i = 1 * this.addQian.text;
                            h.AddProp(1, i), this.destroy(), SdkUtil.TDEvent("视频完成推送加钱")
                        }
                    }.bind(this))
                })
            }

            onDisable() {
            }
        }

        class G extends Laya.Scene {
            constructor() {
                super()
            }

            onEnable() {
                this.tiaoGuan.visiable = !1, this.fangQi.visiable = !1, this.skeleton = new Laya.Skeleton, this.addChild(this.skeleton), this.skeleton.pos(this.width / 2, this.height / 2 + 60), this.skeleton.load("res/longgu/win_fail.sk", Laya.Handler.create(this, function () {
                    this.skeleton.play("fail_01", !1), this.skeleton.on(Laya.Event.STOPPED, this, function () {
                        this.skeleton.play("fail_02", !0)
                    })
                })), Laya.timer.once(1e3, this, function () {
                    this.tiaoGuan.visiable = !0, this.fangQi.visiable = !0
                }), window.SdkUtil.TDGuanQia && window.SdkUtil.TDGuanQia(3, h.GetUserData("showLv")),
                window.SdkUtil.ShowBanner && window.SdkUtil.ShowBanner(), window.SdkUtil.ShowAddIcon && window.SdkUtil.ShowAddIcon(),
                window.SdkUtil.ShowChaPing && window.SdkUtil.ShowChaPing(), SdkUtil.TDEvent(h.GetUserData("showLv") + "游戏失败页面"),
                    D.PlayMusic("Fail", 1), this.tiaoGuan.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("失败页面复活视频点击"),
                        window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (h.SetUserData("showLv", h.GetUserData("showLv") + 1), this.destroy(),
                            r.ShowUIPanel("Second"), SdkUtil.TDEvent("失败页面复活视频完成"))
                    }.bind(this)));
                }), this.fangQi.on(Laya.Event.CLICK, this, function () {
                    this.destroy(), D.PlaySound("Btn"), r.ShowUIPanel("Second");
                    window.HUHU_showInterstitialAd();
                });
            }

            onDisable() {
                Laya.timer.clearAll(this), window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner()
            }
        }

        class I extends Laya.Scene {
            constructor() {
                super()
            }

            onEnable() {
                window.SdkUtil.ADInit(!1), this.loadValue = 0, this.curValue = 0, this.onUpdate(), Laya.timer.frameLoop(1, this, this.onUpdate), window.SdkUtil.LoadSubpackage ? (this.loadValue = 1, window.SdkUtil.LoadSubpackage(function () {
                    this.LoadConfig()
                }.bind(this))) : this.LoadConfig();
                var t = ["font01", "font02", "font03", "font04", "font05"];
                for (let i = 0; i < t.length; i++) {
                    let e = new Laya.BitmapFont;
                    e.loadFont("First/Font/" + t[i] + ".fnt", new Laya.Handler(this, function () {
                        Laya.Text.registerBitmapFont(t[i], e)
                    }))
                }
            }

            onDisable() {
            }

            onUpdate() {
                this.curValue += .01, this.curValue > this.loadValue && (this.curValue = this.loadValue), this.curValue >= 1 && (this.curValue = 0), this.jiaZaiTiao.width = 450 * this.curValue
            }

            LoadConfig() {
                var t = [];
                t.length > 0 ? Laya.loader.load(t, Laya.Handler.create(this, function () {
                    h.GetData(), this.LoadModels()
                })) : (h.GetData(), this.LoadModels())
            }

            LoadModels() {
                this.loadValue = 1, Laya.Sprite3D.load("res/Scene/Conventional/models.lh", Laya.Handler.create(this, function (t) {
                    if (D.models = t, D.models) {
                        D.guanKaLv = h.GetGuangKalv();
                        var i = "res/Scene/Conventional/Level" + D.guanKaLv + ".ls";
                        D.loadScene(i, function () {
                            this.StartGame()
                        }.bind(this))
                    } else this.LoadModels()
                }))
            }

            StartGame() {
                Laya.timer.clearAll(this), r.ShowUIPanel("GameRun", !0, !1), window.SdkUtil.ReportMonitor && window.SdkUtil.ReportMonitor(1)
            }
        }

        class V extends Laya.Scene {
            constructor() {
                super(), this.unlockpiFuIndexList = new Array, this.timerNum = 30, this.skeleton
            }

            onOpened(t) {
                if (r.gameUI = this, 1 == t) {
                    var i = new Date,
                        e = i.getMonth() + 1,
                        a = i.getFullYear() + "年" + e + "月" + i.getDate() + "日";
                    h.GetUserData("curDay") != a && h.GetUserData("signNum") < 7 && r.ShowUIPanel("Sign", !1)
                }
                this.Init(), this.shop.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), r.ShowUIPanel("Shop", !1)
                }), this.addQianBtn.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), SdkUtil.TDEvent("视频点击主页加钱"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (h.AddProp(1, 2e3), SdkUtil.TDEvent("视频完成主页加钱"))
                    }.bind(this))
                }), D.PlayMusic("BGM");
                this.btn_sound.on(Laya.Event.CLICK, this, function () {
                    Laya.SoundManager.muted = !Laya.SoundManager.muted;
                    if(Laya.SoundManager.muted){
                        this.btn_sound.skin= "sound_off.png";
                    }
                    else{
                        this.btn_sound.skin= "sound_on.png";
                    }
                })
            }

            onDisable() {
                Laya.timer.clearAll(this), r.gameUI = null, window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner()
            }

            Init() {
                this.StartGame(), this.lvQian.text = h.GetUserData("showLv"), this.youXiZhong.visible = !1, this.jiShaBg.visible = !1, this.sheJiTiShi.visible = !1, this.qian.text = h.GetUserData("Gold"), Laya.timer.loop(10, this, function () {
                    this.qian.text = h.GetUserData("Gold"), this.jiShaNum.text = D.jiShaNum
                })
            }

            showSheJiTiShi(t) {
                var i = new Laya.Vector4;
                D.mainCamera.worldToViewportPoint(t, i), this.sheJiTiShi.x = i.x, this.sheJiTiShi.y = i.y - 50, this.sheJiTiShi.visible = !0
            }

            hideSheJiTiShi(t) {
                this.sheJiTiShi.visible = !1
            }

            showZhiYin1() {
                this.zhiYin1.visible = !0, this.shou.visible = !0
            }

            hideZhiYin1() {
                this.zhiYin1.visible = !1, this.shou.visible = !1
            }

            showAnNiu() {
                this.anNiu.visible = !0
            }

            hideAnNiu() {
                this.anNiu.visible = !1
            }

            beginHide() {
                window.SdkUtil.luzhiKaishi && window.SdkUtil.luzhiKaishi(), this.anNiu.visible = !1,
                    this.youXiZhong.visible = !0, this.end.visible = !1, this.zhiYin1.visible = !1, this.jiShaBg.visible = !0, this.guanKaBg.visible = !1;
                window.HUHU_showInterstitialAd();
            }

            hideAll() {
                this.youXiZhong.visible = !1, this.anNiu.visible = !1, this.end.visible = !1
            }

            StartGame() {
                var t = h.GetUserData("piFuType");
                this.unlockpiFuIndexList.length = 0;
                for (let i = 1; i <= 6; i++) 0 == t[i] && this.unlockpiFuIndexList.push(i);
                D.curLevelManager.CreatePlayer(), window.SdkUtil.TDGuanQia(1, h.GetUserData("showLv"));

            }
        }

        class A extends Laya.Scene {
            constructor() {
                super(), this.show
            }

            onOpened(t) {
                this.closeBtn.visiable = !1, this.getBtn.visiable = !1, this.skeleton = new Laya.Skeleton, this.addChild(this.skeleton), this.skeleton.pos(this.width / 2, this.height / 2), this.skeleton.load("res/longgu/tuisong.sk", Laya.Handler.create(this, function () {
                    this.skeleton.play(0, !0)
                })), Laya.timer.once(1e3, this, function () {
                    this.closeBtn.visiable = !0, this.getBtn.visiable = !0
                }), this.show = Laya.Sprite3D.instantiate(D.models.getChildByName("showCamera"), D.curScene), this.updateShow(t - 1), this.show.transform.position = new Laya.Vector3(1e4, 1e4, 1e4);
                var i = this.show.getChildByName("camera").getChildByName("Camera");
                i.renderTarget = new Laya.RenderTexture(720, 600, Laya.RenderTextureFormat.R8G8B8A8), i.clearFlag = 0, i.clearColor = new Laya.Vector4(0, 0, 0, 0);
                var e = new Laya.Texture(i.renderTarget, Laya.Texture.DEF_UV);
                this.showBg.graphics.drawTexture(e), this.closeBtn.on(Laya.Event.CLICK, this, function (t) {
                    D.PlaySound("Btn"), null != D.curPlayerControl && (r.pushUI = 0, D.curPlayerControl.mouseDown(t)), this.destroy()
                }), this.getBtn.on(Laya.Event.CLICK, this, function (i) {
                    D.PlaySound("Btn"), SdkUtil.TDEvent("视频点击推送换皮肤"), window.SdkUtil.ShowVideo(function (e) {
                        1 == e && (null != D.curPlayerControl && (r.pushUI = 0, D.currentPiFuType = t, D.curPlayerControl.updateShopYifu(t - 1), D.curPlayerControl.mouseDown(i)), this.destroy(), SdkUtil.TDEvent("视频完成推送换皮肤"))
                    }.bind(this))
                }), null != this.ADPanel && SdkUtil.ShowNeiZhiAD && SdkUtil.ShowNeiZhiAD(this.ADPanel, 1)
            }

            updateShow(t) {
                var i = this.show.getChildByName("Qiang");
                for (let e = 0; e < 6; e++) i.getChildAt(e).active = t == e
            }

            onDisable() {
                null != this.show && this.show.destroy()
            }
        }

        class F extends Laya.Scene {
            constructor() {
                super(), this.tiaoAllWidth
            }

            onEnable() {
                this.loadScene()
            }

            loadScene() {
                D.guanKaLv = h.GetGuangKalv();
                var t = "res/Scene/Conventional/Level" + D.guanKaLv + ".ls";
                D.loadScene(t, function () {
                    Laya.timer.once(1, this, function () {
                        this.destroy(), r.ShowUIPanel("GameRun", !0, !0)
                    })
                }.bind(this))
            }
        }

        class M extends Laya.Scene {
            constructor() {
                super(), this.pageYe = 0, this.show
            }

            onEnable() {
                window.SdkUtil.ShowBanner && window.SdkUtil.ShowBanner(), window.SdkUtil.ShowChaPing && window.SdkUtil.ShowChaPing(), this.show = Laya.Sprite3D.instantiate(D.models.getChildByName("showCamera"), D.curScene), this.updateShow(D.piFuType - 1), this.show.transform.position = new Laya.Vector3(1e4, 1e4, 1e4);
                var t = this.show.getChildByName("camera").getChildByName("Camera");
                t.renderTarget = new Laya.RenderTexture(720, 600, Laya.RenderTextureFormat.R8G8B8A8), t.clearFlag = 0, t.clearColor = new Laya.Vector4(0, 0, 0, 0);
                var i = new Laya.Texture(t.renderTarget, Laya.Texture.DEF_UV);
                this.showBg.graphics.drawTexture(i), this.updateUI();
                for (let t = 1; t <= this.bg.numChildren; t++) this["shiYong" + t].on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), D.piFuType = t, null != D.curPlayerControl && D.curPlayerControl.updateShopYifu(D.piFuType - 1), D.currentPiFuType = -1, this.updateUI(), this.updateShow(D.piFuType - 1), h.savePiFuTypeNum(D.piFuType)
                }), this["xiaoHao" + t].on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn");
                    var i = 1 * this["xiaoHaoNum" + t].text;
                    h.IsCanLessProp(1, i) ? (h.LessProp(1, i), D.piFuType = t, null != D.curPlayerControl && D.curPlayerControl.updateShopYifu(D.piFuType - 1), D.currentPiFuType = -1, h.SavePiFuTypeList(D.piFuType), h.savePiFuTypeNum(D.piFuType), this.updateUI(), this.updateShow(D.piFuType - 1)) : r.ShowUIPanel("BuyGold", !1)
                });
                this.fangQi.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), this.destroy()
                }), this.qian.text = h.GetUserData("Gold"), Laya.timer.loop(10, this, function () {
                    this.qian.text = h.GetUserData("Gold")
                });
                window.HUHU_showInterstitialAd();
            }

            updateUI() {
                this.xiaoHaoNum1.text = 0, this.xiaoHaoNum2.text = 2e3, this.xiaoHaoNum3.text = 5e3, this.xiaoHaoNum4.text = 5e3, this.xiaoHaoNum5.text = 5e3, this.xiaoHaoNum6.text = 5e3;
                var t = h.GetUserData("piFuType");
                for (let e = 1; e <= 6; e++)
                    if (null != t[e])
                        if (1 == t[e]) {
                            var i = "btn" + e;
                            this.bg.getChildByName(i).getChildByName("gouMai").visible = !1, this.bg.getChildByName(i).getChildByName("yongYou").visible = !0, -1 == D.currentPiFuType ? D.piFuType == e ? (this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !1) : (this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !1,
                                this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !0) : D.currentPiFuType == e ? (this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !1) : (this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !1, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !0)
                        } else i = "btn" + e, D.currentPiFuType != e ? (this.bg.getChildByName(i).getChildByName("gouMai").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").visible = !1, this.bg.getChildByName(i).getChildByName("gouMai").getChildByName("shiPin").visible = !1, this.bg.getChildByName(i).getChildByName("gouMai").getChildByName("xiaoHao").visible = !0) : (this.bg.getChildByName(i).getChildByName("gouMai").visible = !1, this.bg.getChildByName(i).getChildByName("yongYou").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !1);
                    else i = "btn" + e, D.currentPiFuType != e ? (this.bg.getChildByName(i).getChildByName("gouMai").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").visible = !1, this.bg.getChildByName(i).getChildByName("gouMai").getChildByName("shiPin").visible = !1, this.bg.getChildByName(i).getChildByName("gouMai").getChildByName("xiaoHao").visible = !0) : (this.bg.getChildByName(i).getChildByName("gouMai").visible = !1, this.bg.getChildByName(i).getChildByName("yongYou").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("yiYong").visible = !0, this.bg.getChildByName(i).getChildByName("yongYou").getChildByName("shiYong").visible = !1)
            }

            updateShow(t) {
                var i = this.show.getChildByName("Qiang");
                for (let e = 0; e < 6; e++) i.getChildAt(e).active = t == e
            }

            onDisable() {
                window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner(), null != this.show && this.show.destroy()
            }
        }

        class _ extends Laya.Scene {
            constructor() {
                super(), this.qianDaoQian = 100
            }

            onEnable() {
                window.SdkUtil.ShowBanner && window.SdkUtil.ShowBanner();
                var t = new Date,
                    i = t.getMonth() + 1,
                    e = t.getFullYear() + "年" + i + "月" + t.getDate() + "日";
                this.initQianDaoFun(), this.shuangBei.on(Laya.Event.CLICK, this, function () {
                    if (D.PlaySound("Btn"), h.GetUserData("curDay") == e) return r.ShowGameTipUI("Today claimed!"), void this.destroy();
                    window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("签到页面视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (h.GetUserData("curDay") != e ? (h.AddProp(1, 2 * this.qianDaoQian), h.SetUserData("curDay", e), h.SetUserData("signNum", h.GetUserData("signNum") + 1), r.ShowGameTipUI("You claimed!")) : r.ShowGameTipUI("Today claimed!"), this.destroy(), SdkUtil.TDEvent("签到页面视频完成"))
                    }.bind(this)))
                }), this.qianDao.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), h.GetUserData("curDay") != e ? (h.AddProp(1, this.qianDaoQian), h.SetUserData("curDay", e), h.SetUserData("signNum", h.GetUserData("signNum") + 1), r.ShowGameTipUI("You claimed!"), r.ShowGameTipUI("You claimed!")) : r.ShowGameTipUI("Today claimed!"), this.destroy()
                });
                window.HUHU_showInterstitialAd();
            }

            initQianDaoFun() {
                var t = h.GetUserData("signNum") + 1;
                for (let e = 1; e <= this.allDay.numChildren; e++) {
                    var i = "day" + e;
                    this["dayQian" + e].text = 50 * e + 50, h.GetUserData("signNum") >= e ? this.allDay.getChildByName(i).getChildByName("yiQian").visible = !0 : (this.allDay.getChildByName(i).getChildByName("yiQian").visible = !1, t <= 7 && t == e && (this.qianDaoQian = 1 * this["dayQian" + e].text))
                }
            }

            onDisable() {
                window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner()
            }
        }

        class Z extends Laya.Scene {
            constructor() {
                super(), this.show
            }

            onEnable() {
                this.init()
            }

            init() {
                this.shuangBei.visiable = !1, this.fangQi.visiable = !1, this.skeleton = new Laya.Skeleton, this.addChild(this.skeleton),
                    this.skeleton.pos(this.width / 2, this.height / 2 + 60),
                    this.skeleton.load("res/longgu/win_fail.sk", Laya.Handler.create(this, function () {
                    this.skeleton.play("win_01", !1), this.skeleton.on(Laya.Event.STOPPED, this, function () {
                        this.skeleton.play("win_02", !0)
                    })
                })), Laya.timer.once(1e3, this, function () {
                    this.shuangBei.visiable = !0, this.fangQi.visiable = !0
                }), SdkUtil.IsShowShareBtn && SdkUtil.IsShowShareBtn(), window.SdkUtil.TDGuanQia && window.SdkUtil.TDGuanQia(2, h.GetUserData("showLv")),
                window.SdkUtil.ShowBanner && window.SdkUtil.ShowBanner(), window.SdkUtil.ShowAddIcon && window.SdkUtil.ShowAddIcon(),
                window.SdkUtil.ShowChaPing && window.SdkUtil.ShowChaPing(), null != this.ADPanel && SdkUtil.ShowNeiZhiAD && SdkUtil.ShowNeiZhiAD(this.ADPanel, 2),
                    D.PlayMusic("win", 1), this.addQian.text = 50 * h.GetUserData("showLv"), h.SetUserData("showLv", h.GetUserData("showLv") + 1),
                    this.shuangBei.on(Laya.Event.CLICK, this, function () {
                    D.PlaySound("Btn"), window.SdkUtil.ShowVideo && (SdkUtil.TDEvent("胜利页面三倍视频点击"), window.SdkUtil.ShowVideo(function (t) {
                        1 == t && (h.AddProp(1, 2 * this.addQian.text), this.destroy(), r.ShowUIPanel("Second"), r.ShowGameTipUI("You claimx2!"),
                            SdkUtil.TDEvent("胜利页面双倍视频完成"))
                    }.bind(this)));
                }), this.fangQi.on(Laya.Event.CLICK, this, function () {
                    h.AddProp(1, 1 * this.addQian.text), D.PlaySound("Btn"), r.ShowUIPanel("Second"), this.destroy();
                    window.HUHU_showInterstitialAd();
                });
            }

            onDisable() {
                Laya.timer.clearAll(this), window.SdkUtil.CloseBanner && window.SdkUtil.CloseBanner(), window.SdkUtil.TDGuanQia(1, h.GetUserData("showLv"))
            }
        }

        class W {
            static init() {
                let t = Laya.ClassUtils.regClass;
                t("PanelBox.js", U),
                    t("PanelBuyGold.js", k),
                    t("PanelFail.js", G),
                    t("PanelFirst.js", I),
                    t("PanelGameRun.js", V),
                    t("PanelPush.js", A),
                    t("PanelSecond.js", F),
                    t("PanelShop.js", M),
                    t("PanelSign.js", _),
                    t("PanelWin.js", Z)
            }
        }

        W.width = 720, W.height = 1280, W.scaleMode = "fixedwidth", W.screenMode = "vertical", W.alignV = "middle", W.alignH = "center", W.startScene = "UIPanel/Shop.scene", W.sceneRoot = "", W.debug = !1, W.stat = !1, W.physicsDebug = !1, W.exportSceneToJson = !0, W.init(), new class {
            constructor() {
                window.Laya3D ? Laya3D.init(W.width, W.height) : Laya.init(W.width, W.height, Laya.WebGL), Laya.Physics && Laya.Physics.enable(), Laya.DebugPanel && Laya.DebugPanel.enable(), Laya.stage.scaleMode = W.scaleMode, Laya.stage.screenMode = W.screenMode, Laya.stage.alignV = W.alignV, Laya.stage.alignH = W.alignH, Laya.URL.exportSceneToJson = W.exportSceneToJson, (W.debug || "true" == Laya.Utils.getQueryString("debug")) && Laya.enableDebugPanel(), W.physicsDebug && Laya.PhysicsDebugDraw && Laya.PhysicsDebugDraw.enable(), W.stat && Laya.Stat.show(), Laya.alertGlobalError(!0), Laya.ResourceVersion.enable("version.json", Laya.Handler.create(this, this.onVersionLoaded), Laya.ResourceVersion.FILENAME_VERSION)
            }

            onVersionLoaded() {
                Laya.AtlasInfoManager.enable("fileconfig.json", Laya.Handler.create(this, this.onConfigLoaded))
            }

            onConfigLoaded() {
                // @ts-ignore
                if (typeof minigame !== 'undefined') {
                    let that = this;
                    //初始化 minigame sdk
                    // @ts-ignore
                    minigame.initializeAsync()
                        .then(function () {
                            console.log("FB initializeAsync");
                            that.startMiniGameSDK();
                        });
                }
            }
            // 启动minigame sdk
            startMiniGameSDK() {
                // @ts-ignore
                if (typeof minigame !== 'undefined') {
                    //@ts-ignore
                    minigame.setLoadingProgress(100);
                    //@ts-ignore
                    minigame.startGameAsync()
                        .then(function () {
                            //加载IDE指定的场景，这⾥假定第⼀个场景名称是startScene
                            W.startScene && Laya.Scene.open("UIPanel/First.scene");
                            window.HUHU_showBannerAd();
                        })
                        .catch(function (e) {
                            console.info("startGameAsync error: " + e);
                        });
                }
            }
        }
    }();