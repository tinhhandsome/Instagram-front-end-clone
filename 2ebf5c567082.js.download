__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var s = r(d[3]).connect(
      function (s, t) {
        return {
          users: r(d[0]).getFeedAysfUsers(s, t),
          shouldRenderContactImportUpsell: r(
            d[1]
          ).shouldRenderContactImportUpsell(s, "CHAINING_LIST_ITEM"),
        };
      },
      function (s) {
        return {
          onSuggestionDismissed: function (t) {
            s(r(d[2]).dismissFeedAysfSuggestion(t));
          },
        };
      }
    )(i(d[4]));
    e.default = s;
  },
  13238272,
  [10289241, 10289242, 10289278, 5, 13107202]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0]).createSelector(
      function (t) {
        return t.contactImport.ids;
      },
      function (t) {
        return t.toArray();
      }
    );
    (e.getContactUserIDs = t),
      (e.getContactUsers = function (n) {
        return (r(d[1]).getUsersByIds(n, t(n)) || []).map(function (t) {
          return {
            user: t,
            relationship: r(d[2]).getRelationship(n.relationships, t.id),
          };
        });
      }),
      (e.shouldRenderContactImportUpsell = function (t, n) {
        var s,
          c = t.contactImport.canImportContacts,
          o = !t.contactImport.upsellStatus.get("chainingListUpsellDismissed"),
          u = !t.contactImport.upsellStatus.get(
            "emptyFeedCarouselCardDismissed"
          ),
          l =
            null === (s = t.settings.privacyAndSecurityData) || void 0 === s
              ? void 0
              : s.allowContactsSync.value;
        switch (n) {
          case "CONTACTS_LIST":
          case "NO_CONTACTS":
          case "NUX":
            return c;
          case "LIST_ITEM":
            return c && !l;
          case "EMPTY_FEED_CAROUSEL_CARD":
            return u && c && !l;
          case "CHAINING_LIST_ITEM":
            return o && c && !l;
          default:
            return !1;
        }
      });
  },
  10289242,
  [9, 9895966, 10158088]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var s = r(d[1])(1702),
      o = function (o) {
        a(d[2]).useEffect(
          function () {
            var s = o.position,
              t = o.trackingToken,
              n = o.type;
            null != s &&
              r(d[3]).logNetEgoEvent({
                containerModule: r(d[3]).NETEGO_CONTAINER_MODULES.feed,
                eventName: "instagram_netego_impression",
                isFromNeedyUser: !0,
                position: s,
                trackingToken: t,
                type: n,
              });
          },
          [o.position]
        );
        var t = o.className,
          n = o.impressionModule,
          l = o.onSuggestionDismissed,
          u = o.users,
          _ = o.shouldRenderContactImportUpsell,
          c = o.variant;
        return a(d[2]).createElement(i(d[4]), {
          analyticsContext: r(d[5]).CONNECTIONS_CONTAINER_MODULES.feed_timeline,
          chainingSuggestions: u,
          className: i(d[6])(
            t,
            (c === r(d[7]).VARIANTS.narrow ? "bq3Mi" : "") +
              " " +
              (c === r(d[7]).VARIANTS.wide ? "vboSt" : "") +
              " " +
              (r(d[8]).isMobile() ? "D_6tu" : "") +
              " " +
              (r(d[8]).isMobile() ? "" : "_6E_wP")
          ),
          clickPoint: "feed_h_scroll_suggested_user_list",
          impressionModule: n,
          isSmallScreen: c === r(d[7]).VARIANTS.narrow,
          onSuggestionDismissed: l,
          seeAllHref: r(d[9]).DISCOVER_PEOPLE_PATH,
          shouldRenderContactImportUpsell: _,
          showDescription: !0,
          title: s,
        });
      };
    o.defaultProps = { impressionModule: r(d[5]).VIEW_MODULES.hscroll_feed };
    var t = o;
    e.default = t;
  },
  13107202,
  [
    13107203,
    9895940,
    3,
    13107204,
    13107205,
    10158213,
    9895958,
    13107206,
    9764909,
    10158338,
  ]
);
__d(function () {}, 13107203, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    (e.NETEGO_CONTAINER_MODULES = { feed: "feed" }),
      (e.logNetEgoEvent = function (t) {
        var o = t.containerModule,
          n = t.eventName,
          _ = t.isFromNeedyUser,
          c = t.position,
          l = t.trackingToken,
          s = t.type,
          v = {
            is_from_needy_user: Boolean(_),
            position: c,
            device_model: r(d[0]).getBrowserString(),
            device_os: "Web",
            gap_to_last_netego: -1,
            primary_locale: r(d[1]).getLocale(),
            deviceid: r(d[2]).getDeviceOrMachineId(),
            tracking_token: l,
            type: s,
          };
        r(d[3]).logPigeonEvent(
          r(d[4]).createEvent(n, r(d[3]).getExtra(v), { module: o })
        );
      });
  },
  13107204,
  [9764909, 9764880, 9764883, 9764900, 9764889]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    function t(t, n) {
      var o = Object.keys(t);
      if (Object.getOwnPropertySymbols) {
        var l = Object.getOwnPropertySymbols(t);
        n &&
          (l = l.filter(function (n) {
            return Object.getOwnPropertyDescriptor(t, n).enumerable;
          })),
          o.push.apply(o, l);
      }
      return o;
    }
    function n(n) {
      for (var o = 1; o < arguments.length; o++) {
        var l = null != arguments[o] ? arguments[o] : {};
        o % 2
          ? t(l, !0).forEach(function (t) {
              i(d[1])(n, t, l[t]);
            })
          : Object.getOwnPropertyDescriptors
          ? Object.defineProperties(n, Object.getOwnPropertyDescriptors(l))
          : t(l).forEach(function (t) {
              Object.defineProperty(
                n,
                t,
                Object.getOwnPropertyDescriptor(l, t)
              );
            });
      }
      return n;
    }
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var o = r(d[2])(2946),
      l = { cardWidth: 156, gapWidth: 5, gutterWidth: 20, height: 208 },
      s = { cardWidth: 176, gapWidth: 24, gutterWidth: 24, height: 208 },
      c = (function (t) {
        function c(n) {
          var o;
          return (
            (o = t.call(this, n) || this),
            (o.$FollowChainingList3 = function () {
              (o.$FollowChainingList1 = !0),
                o.$FollowChainingList4(),
                o.props.onScrollEnter && o.props.onScrollEnter();
            }),
            (o.$FollowChainingList5 = function () {
              (o.$FollowChainingList1 = !1),
                o.props.onScrollLeave && o.props.onScrollLeave();
            }),
            (o.$FollowChainingList6 = function (t) {
              var n = t.leftPct,
                l = t.rightPct;
              (o.$FollowChainingList7 = Math.max(0, Math.floor(n))),
                (o.$FollowChainingList8 = Math.max(0, Math.floor(l))),
                o.$FollowChainingList4();
            }),
            (o.$FollowChainingList1 = !1),
            (o.$FollowChainingList2 = {}),
            o
          );
        }
        i(d[3])(c, t);
        var h = c.prototype;
        return (
          (h.$FollowChainingList4 = function () {
            if (
              this.$FollowChainingList1 &&
              null != this.$FollowChainingList7 &&
              null != this.$FollowChainingList8 &&
              null != this.props.chainingSuggestions
            )
              for (
                var t = this.$FollowChainingList7;
                t <= this.$FollowChainingList8;
                ++t
              ) {
                var o = this.props.chainingSuggestions[t];
                if (null != o && !this.$FollowChainingList2[o.id]) {
                  var l = this.props.impressionModule,
                    s = {
                      targetId: o.id,
                      containerModule: this.props.analyticsContext,
                      position: t,
                      viewModule: l,
                    };
                  l === r(d[4]).VIEW_MODULES.web_profile_chaining
                    ? r(d[4]).logConnectionAction(
                        n({ eventName: "similar_user_impression" }, s)
                      )
                    : (l !== r(d[4]).VIEW_MODULES.hscroll_feed &&
                        l !== r(d[4]).VIEW_MODULES.end_of_feed) ||
                      r(d[4]).logConnectionAction(
                        n({ eventName: "recommended_user_impression" }, s)
                      ),
                    (this.$FollowChainingList2[o.id] = !0);
                }
              }
          }),
          (h.render = function () {
            var t = this.props,
              n = t.analyticsContext,
              c = t.chainingFailed,
              h = t.chainingSuggestions,
              p = t.className,
              u = t.clickPoint,
              f = t.impressionModule,
              w = t.isSmallScreen,
              C = t.onRetryClicked,
              L = t.onSuggestionDismissed,
              E = t.overscan,
              v = t.seeAllHref,
              y = t.shouldRenderContactImportUpsell,
              F = t.showDescription,
              $ = t.title,
              S = w ? l : s,
              O =
                h &&
                h.map(function (t, o) {
                  return a(d[5]).createElement(i(d[6]), {
                    analyticsContext: n,
                    clickPoint: u,
                    impressionModule: f,
                    isSmallScreen: w,
                    key: t.id,
                    onDismissed: L,
                    position: o,
                    showDescription: F,
                    user: t,
                  });
                });
            return (
              null != O &&
                y &&
                O.splice(
                  2,
                  0,
                  a(d[5]).createElement(i(d[7]), {
                    analyticsContext: n,
                    key: "contactImport",
                    variant: "CHAINING_LIST_ITEM",
                  })
                ),
              null != O &&
                (O = O.map(function (t) {
                  return a(d[5]).createElement(
                    r(d[8]).Box,
                    {
                      alignItems: "center",
                      height: S.height,
                      key: t.key,
                      width: S.cardWidth + S.gapWidth,
                    },
                    a(d[5]).createElement(
                      r(d[8]).Box,
                      { width: S.cardWidth },
                      t
                    )
                  );
                })),
              a(d[5]).createElement(
                i(d[9]),
                {
                  className: i(d[10])(
                    p,
                    "ccgHY " + (w ? "l9Ww0" : "") + " " + (w ? "" : "GZkEI")
                  ),
                  onScrollEnter: this.$FollowChainingList3,
                  onScrollLeave: this.$FollowChainingList5,
                },
                !0 !== c &&
                  !h &&
                  a(d[5]).createElement(
                    "div",
                    { className: "_7AQG4" },
                    a(d[5]).createElement("p", null, o)
                  ),
                !0 === c &&
                  a(d[5]).createElement(i(d[11]), {
                    className: "fNpwd",
                    errorText: r(d[2])(76),
                    onRetry: i(d[12])(C),
                  }),
                !0 !== c &&
                  h &&
                  a(d[5]).createElement(
                    "div",
                    { className: "EM8Od" },
                    a(d[5]).createElement("span", { className: "Rebts" }, $),
                    null != v &&
                      "" !== v &&
                      a(d[5]).createElement(i(d[13]), {
                        href: v,
                        onClick: this.props.onSeeAllClicked,
                      })
                  ),
                !0 !== c &&
                  h &&
                  null != O &&
                  a(d[5]).createElement(
                    r(d[8]).Box,
                    { height: S.height },
                    a(d[5]).createElement(
                      i(d[14]),
                      {
                        gutterWidth: Math.max(
                          0,
                          S.gutterWidth - S.gapWidth / 2
                        ),
                        itemWidth: S.cardWidth + S.gapWidth,
                        onVisibilityChange: this.$FollowChainingList6,
                        overscan: E,
                      },
                      O
                    )
                  )
              )
            );
          }),
          c
        );
      })(a(d[5]).Component);
    c.defaultProps = {
      shouldRenderContactImportUpsell: !1,
      showDescription: !1,
    };
    var h = c;
    e.default = h;
  },
  13107205,
  [
    13107207,
    9764888,
    9895940,
    9764914,
    10158213,
    3,
    13107208,
    10289247,
    9895962,
    12517379,
    9895958,
    12386336,
    9895943,
    10289244,
    13107209,
  ]
);
__d(function () {}, 13107207, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var o = (function (o) {
        function l() {
          for (var l, t = arguments.length, n = new Array(t), s = 0; s < t; s++)
            n[s] = arguments[s];
          return (
            (l = o.call.apply(o, [this].concat(n)) || this),
            (l.$FollowCard4 = function (o) {
              l.$FollowCard3("avatar"), o.stopPropagation();
            }),
            (l.$FollowCard5 = function (o) {
              l.$FollowCard3("username"),
                l.$FollowCard1(
                  l.$FollowCard2()
                    ? "similar_username_tapped"
                    : "recommended_username_tapped"
                ),
                o.stopPropagation();
            }),
            (l.$FollowCard6 = function (o) {
              l.$FollowCard3("follow"),
                l.$FollowCard1(
                  l.$FollowCard2()
                    ? "similar_user_follow_button_tapped"
                    : "recommended_follow_button_tapped"
                ),
                o.stopPropagation();
            }),
            (l.$FollowCard7 = function () {
              var o = l.props,
                t = o.onDismissed,
                n = o.user.id;
              l.$FollowCard1(
                l.$FollowCard2()
                  ? "similar_user_dismiss_tapped"
                  : "recommended_user_dismissed"
              ),
                t && t(n);
            }),
            (l.$FollowCard8 = function () {
              var o = l.props.user.username;
              (null != o && "" !== o) || i(d[2])(0);
              var t = r(d[3]).buildUserLink(o);
              l.props.history.push(t);
            }),
            l
          );
        }
        i(d[1])(l, o);
        var t = l.prototype;
        return (
          (t.$FollowCard1 = function (o) {
            var l = this.props,
              t = l.analyticsContext,
              n = l.impressionModule,
              s = l.position,
              u = l.user;
            r(d[4]).logConnectionAction({
              eventName: o,
              position: s,
              targetId: u.id,
              containerModule: t,
              viewModule: n,
            });
          }),
          (t.$FollowCard2 = function () {
            return (
              this.props.impressionModule ===
              r(d[4]).VIEW_MODULES.web_profile_chaining
            );
          }),
          (t.$FollowCard3 = function (o) {
            r(d[5]).logAction_DEPRECATED("chainingClick", {
              source: this.props.analyticsContext,
              target: o,
            });
          }),
          (t.$FollowCard9 = function (o) {
            return o.length < 33 ? o : o.substr(0, 30) + "…";
          }),
          (t.$FollowCard10 = function () {
            var o = this.props,
              l = o.showDescription,
              t = o.user.suggestionDescription;
            return l && null != t;
          }),
          (t.$FollowCard11 = function () {
            var o = this.props,
              l = o.isSmallScreen,
              t = o.user,
              n = t.profilePictureUrl,
              s = t.username;
            return (
              (null != n && "" !== n) || i(d[2])(0),
              a(d[6]).createElement(i(d[7]), {
                canTabFocus: !1,
                isLink: !0,
                onClick: this.$FollowCard4,
                profilePictureUrl: n,
                size: l ? 77 : 54,
                username: s,
              })
            );
          }),
          (t.$FollowCard12 = function () {
            var o = this.props.user,
              l = o.fullName,
              t = o.isVerified,
              n = o.username;
            return (
              (null != n && "" !== n) || i(d[2])(0),
              null != t || i(d[2])(0),
              a(d[6]).createElement(
                a(d[6]).Fragment,
                null,
                a(d[6]).createElement(
                  i(d[8]),
                  {
                    className: "Qj3-a",
                    onClick: this.$FollowCard5,
                    username: n,
                  },
                  !0 === this.$FollowCard10() &&
                    null != l &&
                    "" !== l &&
                    l.length > 0
                    ? l
                    : n
                ),
                t &&
                  a(d[6]).createElement(
                    r(d[9]).Box,
                    { marginStart: 1 },
                    a(d[6]).createElement(r(d[9]).VerifiedBadge, null)
                  )
              )
            );
          }),
          (t.$FollowCard13 = function () {
            var o = this.props.user,
              l = o.fullName,
              t = o.suggestionDescription;
            return !0 !== this.$FollowCard10()
              ? a(d[6]).createElement(
                  "span",
                  { className: i(d[10])("notranslate", "_7cyhW"), title: l },
                  l
                )
              : a(d[6]).createElement(
                  "span",
                  { className: "_0p1Te", title: t },
                  this.$FollowCard9(t)
                );
          }),
          (t.$FollowCard14 = function () {
            var o = this.props,
              l = o.analyticsContext,
              t = o.clickPoint,
              n = o.user,
              s = n.id,
              u = n.username;
            return a(d[6]).createElement(i(d[11]), {
              analyticsContext: l,
              analyticsExtra: { chn: 1 },
              clickPoint: t,
              fullWidth: !0,
              onClick: this.$FollowCard6,
              userId: s,
              username: u,
            });
          }),
          (t.render = function () {
            var o = this.props,
              l = o.analyticsContext,
              t = o.isSmallScreen,
              n = o.onDismissed;
            return a(d[6]).createElement(i(d[12]), {
              analyticsContext: l,
              icon: this.$FollowCard11(),
              isSmallScreen: t,
              onClick: this.$FollowCard8,
              onDismissed: n ? this.$FollowCard7 : null,
              primaryCta: this.$FollowCard14(),
              primaryText: this.$FollowCard12(),
              secondaryText: this.$FollowCard13(),
            });
          }),
          l
        );
      })(a(d[6]).Component),
      l = r(d[13]).withRouter(o);
    e.default = l;
  },
  13107208,
  [
    13107210,
    9764914,
    9699436,
    9895959,
    10158213,
    9764900,
    3,
    9895946,
    9895947,
    9895962,
    9895958,
    10158212,
    10289255,
    6,
  ]
);
__d(function () {}, 13107210, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]), r(d[1]);
    var t = (function (t) {
      function n() {
        for (var n, o = arguments.length, s = new Array(o), l = 0; l < o; l++)
          s[l] = arguments[l];
        return (
          (n = t.call.apply(t, [this].concat(s)) || this),
          (n.$FollowChainingListItem2 = function (t) {
            var o = n.props.onDismissed;
            n.$FollowChainingListItem1("dismiss"),
              o && o(),
              t.stopPropagation();
          }),
          (n.$FollowChainingListItem3 = function () {
            var t = n.props.onClick;
            n.$FollowChainingListItem1("other"), t && t();
          }),
          n
        );
      }
      i(d[2])(n, t);
      var o = n.prototype;
      return (
        (o.$FollowChainingListItem1 = function (t) {
          this.props.analyticsContext &&
            r(d[3]).logAction_DEPRECATED("chainingClick", {
              source: this.props.analyticsContext,
              target: t,
            });
        }),
        (o.render = function () {
          var t = this.props,
            n = t.icon,
            o = t.isSmallScreen,
            s = t.onDismissed,
            l = t.primaryCta,
            c = t.primaryText,
            p = t.secondaryText;
          return a(d[4]).createElement(
            "div",
            {
              className: "_41KYi",
              onClick: this.$FollowChainingListItem3,
              role: "button",
              tabIndex: "-1",
            },
            a(d[4]).createElement(
              r(d[5]).Box,
              { alignItems: "center", padding: o ? 4 : 5, width: "100%" },
              s &&
                a(d[4]).createElement(
                  "button",
                  {
                    alt: r(d[6])(3620),
                    className: "fUzmR",
                    onClick: this.$FollowChainingListItem2,
                  },
                  a(d[4]).createElement("div", {
                    className:
                      (o ? "coreSpriteDismissSmall" : "") +
                      " " +
                      (o ? "" : "coreSpriteDismissLarge"),
                  })
                ),
              a(d[4]).createElement(
                r(d[5]).Box,
                { marginBottom: o ? 2 : 5 },
                n
              ),
              a(d[4]).createElement(
                r(d[5]).Box,
                {
                  alignItems: "center",
                  direction: "row",
                  justifyContent: "center",
                  marginBottom: 1,
                  width: "100%",
                },
                c
              ),
              a(d[4]).createElement(
                r(d[5]).Box,
                {
                  alignItems: "center",
                  direction: "row",
                  justifyContent: "center",
                  marginBottom: o ? 2 : 3,
                  width: "100%",
                },
                p
              ),
              l
            )
          );
        }),
        n
      );
    })(a(d[4]).Component);
    e.default = t;
  },
  10289255,
  [9895938, 10289261, 9764914, 9764900, 3, 9895962, 9895940]
);
__d(function () {}, 10289261, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0])(2145),
      n = r(d[0])(3340),
      o = r(d[0])(991),
      s = r(d[0])(1632),
      c = r(d[0])(59),
      C = r(d[0])(2842),
      I = r(d[0])(1880),
      l = r(d[0])(3089),
      E = r(d[0])(2938),
      T = r(d[0])(1003),
      _ = function () {
        return (
          i(d[1])._("24") &&
          a(d[2]).createElement(
            r(d[3]).Text.Footnote,
            { color: "ig-secondary-text", textAlign: "left" },
            T,
            a(d[2]).createElement(
              i(d[4]),
              { href: r(d[5]).CONTACT_IMPORT_DATA_POLICY_PATH },
              " ",
              r(d[6]).LEARN_MORE,
              "."
            )
          )
        );
      },
      p = (function (T) {
        function p(t) {
          var n;
          return (
            (n = T.call(this, t) || this),
            (n.$ImportContacts1 = function () {
              i(d[8])(n.props.history).push(
                r(d[5]).DISCOVER_PEOPLE_SUGGESTTED_PATH
              );
            }),
            (n.$ImportContacts4 = function () {
              i(d[8])(n.props.history).push(
                r(d[5]).DISCOVER_PEOPLE_CONTACTS_PATH
              );
            }),
            (n.$ImportContacts5 = function () {
              var t = n.props,
                o = t.onDismissed,
                s = t.variant;
              "CHAINING_LIST_ITEM" === s
                ? r(d[9])
                    .getUserPreferences()
                    .setItem("showContactImportFeedUnitUpsell", !1)
                : "EMPTY_FEED_CAROUSEL_CARD" === s &&
                  r(d[9])
                    .getUserPreferences()
                    .setItem("showContactImportEmptyFeedCarouselUpsell", !1),
                o && o();
            }),
            (n.state = { showLegalDialog: !1 }),
            n
          );
        }
        i(d[7])(p, T);
        var u = p.prototype;
        return (
          (u.$ImportContacts2 = function () {
            var t = this.props,
              n = t.shouldRender;
            switch (t.variant) {
              case "CHAINING_LIST_ITEM":
              case "CONTACTS_LIST":
              case "EMPTY_FEED_CAROUSEL_CARD":
              case "NO_CONTACTS":
              case "NUX":
                return n;
              case "LIST_ITEM":
                return n && this.$ImportContacts3();
              default:
                return !1;
            }
          }),
          (u.$ImportContacts3 = function () {
            switch (this.props.analyticsContext) {
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.discover_people:
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.newsfeed_you:
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.self_following:
                return !0;
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.follow_requests:
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.self_followers:
              case r(d[10]).CONNECTIONS_CONTAINER_MODULES.feed_timeline:
              default:
                return !1;
            }
          }),
          (u.$ImportContacts6 = function () {
            switch (this.props.variant) {
              case "LIST_ITEM":
                return a(d[2]).createElement(r(d[3]).BorderedIcon, {
                  alt: r(d[0])(2592),
                  icon: r(d[3]).ICONS.CONTACT_IMPORT_SM,
                  size: r(d[3]).CORE_CONSTANTS.AVATAR_SIZES.medium,
                });
              case "CHAINING_LIST_ITEM":
              case "CONTACTS_LIST":
              case "EMPTY_FEED_CAROUSEL_CARD":
              case "NUX":
                return a(d[2]).createElement(r(d[3]).BorderedIcon, {
                  alt: r(d[0])(2592),
                  icon: r(d[3]).ICONS.CONTACT_IMPORT,
                  size: 62,
                });
              case "NO_CONTACTS":
                return a(d[2]).createElement(r(d[3]).BorderedIcon, {
                  alt: r(d[0])(1066),
                  icon: r(d[3]).ICONS.USER_OUTLINE_24_GREY9,
                  size: 62,
                });
              default:
                return null;
            }
          }),
          (u.$ImportContacts7 = function () {
            switch (this.props.variant) {
              case "CHAINING_LIST_ITEM":
              case "EMPTY_FEED_CAROUSEL_CARD":
              case "LIST_ITEM":
                return I;
              case "CONTACTS_LIST":
              case "NUX":
                return t;
              case "NO_CONTACTS":
                return s;
              default:
                return null;
            }
          }),
          (u.$ImportContacts8 = function () {
            switch (this.props.variant) {
              case "CHAINING_LIST_ITEM":
              case "EMPTY_FEED_CAROUSEL_CARD":
              case "LIST_ITEM":
                return l;
              case "CONTACTS_LIST":
              case "NUX":
                return o;
              case "NO_CONTACTS":
                return c;
              default:
                return null;
            }
          }),
          (u.$ImportContacts9 = function () {
            var t = this,
              o = this.props,
              s = o.isProcessing,
              c = o.variant;
            switch (c) {
              case "CHAINING_LIST_ITEM":
              case "EMPTY_FEED_CAROUSEL_CARD":
              case "LIST_ITEM":
                return a(d[2]).createElement(
                  r(d[3]).Button,
                  {
                    fullWidth: "CHAINING_LIST_ITEM" === c,
                    loading: s,
                    onClick: function () {
                      t.setState({ showLegalDialog: !0 });
                    },
                  },
                  E
                );
              case "CONTACTS_LIST":
              case "NUX":
                return a(d[2]).createElement(
                  r(d[3]).Button,
                  {
                    fullWidth: !0,
                    large: !0,
                    loading: s,
                    onClick: this.props.onImportContacts,
                  },
                  n
                );
              case "NO_CONTACTS":
                return a(d[2]).createElement(
                  r(d[3]).Button,
                  { borderless: !0, onClick: this.$ImportContacts1 },
                  C
                );
              default:
                return null;
            }
          }),
          (u.$ImportContacts10 = function () {
            var t = this.props,
              o = t.analyticsContext,
              s = t.hideAction,
              c = t.isProcessing,
              C = t.isSmallScreen;
            switch (t.variant) {
              case "NUX":
                return a(d[2]).createElement(i(d[11]), {
                  bodyText: this.$ImportContacts8(),
                  buttonText: n,
                  headerText: this.$ImportContacts7(),
                  hideAction: s,
                  icon: this.$ImportContacts6(),
                  isProcessing: c,
                  onButtonClick: this.props.onImportContacts,
                });
              case "LIST_ITEM":
                return a(d[2]).createElement(
                  r(d[3]).Box,
                  { marginBottom: 1 },
                  a(d[2]).createElement(r(d[3]).ListItem, {
                    action: this.$ImportContacts9(),
                    icon: this.$ImportContacts6(),
                    subtitle: this.$ImportContacts8(),
                    title: a(d[2]).createElement(
                      r(d[3]).Text.BodyEmphasized,
                      null,
                      this.$ImportContacts7()
                    ),
                  })
                );
              case "CHAINING_LIST_ITEM":
                return a(d[2]).createElement(i(d[12]), {
                  analyticsContext: o,
                  icon: this.$ImportContacts6(),
                  isSmallScreen: i(d[8])(C),
                  onClick: this.$ImportContacts4,
                  onDismissed: this.$ImportContacts5,
                  primaryCta: this.$ImportContacts9(),
                  primaryText: a(d[2]).createElement(
                    r(d[3]).Box,
                    { marginBottom: 2 },
                    a(d[2]).createElement(
                      r(d[3]).Text.BodyEmphasized,
                      null,
                      this.$ImportContacts7()
                    )
                  ),
                  secondaryText: a(d[2]).createElement(
                    r(d[3]).Box,
                    { marginBottom: 3 },
                    a(d[2]).createElement(
                      r(d[3]).Text.Footnote,
                      { color: "ig-secondary-text" },
                      this.$ImportContacts8()
                    )
                  ),
                });
              case "EMPTY_FEED_CAROUSEL_CARD":
                return a(d[2]).createElement(r(d[13]).UpsellCard, {
                  body: this.$ImportContacts8(),
                  button: this.$ImportContacts9(),
                  header: this.$ImportContacts7(),
                  icon: this.$ImportContacts6(),
                  onDismiss: this.$ImportContacts5,
                });
              default:
                return a(d[2]).createElement(
                  r(d[3]).Box,
                  {
                    alignItems: "center",
                    justifyContent: "center",
                    marginTop: 15,
                  },
                  a(d[2]).createElement(
                    r(d[3]).Box,
                    {
                      alignItems: "center",
                      justifyContent: "center",
                      padding: 9,
                    },
                    a(d[2]).createElement(
                      r(d[3]).Box,
                      { paddingY: 3 },
                      this.$ImportContacts6()
                    ),
                    a(d[2]).createElement(
                      r(d[3]).Box,
                      { paddingY: 3 },
                      a(d[2]).createElement(
                        r(d[3]).Text.Headline2,
                        null,
                        this.$ImportContacts7()
                      )
                    ),
                    a(d[2]).createElement(
                      r(d[3]).Box,
                      { paddingY: 3 },
                      a(d[2]).createElement(
                        r(d[3]).Text.Body,
                        { color: "ig-secondary-text", textAlign: "center" },
                        this.$ImportContacts8()
                      )
                    ),
                    a(d[2]).createElement(
                      r(d[3]).Box,
                      { paddingY: 3, width: "100%" },
                      this.$ImportContacts9()
                    ),
                    a(d[2]).createElement(
                      r(d[3]).Box,
                      { paddingY: 4 },
                      a(d[2]).createElement(_, null)
                    )
                  )
                );
            }
          }),
          (u.render = function () {
            var t = this;
            return this.$ImportContacts2()
              ? a(d[2]).createElement(
                  a(d[2]).Fragment,
                  null,
                  this.$ImportContacts10(),
                  this.state.showLegalDialog &&
                    a(d[2]).createElement(i(d[14]), {
                      hideIcon: !1,
                      onClose: function () {
                        t.setState({ showLegalDialog: !1 });
                      },
                      onConfirm: this.props.onImportContacts,
                    })
                )
              : null;
          }),
          p
        );
      })(a(d[2]).Component);
    p.defaultProps = {
      hideAction: !1,
      redirectToContactsPage: !0,
      isSmallScreen: !1,
      variant: "CONTACTS_LIST",
    };
    var u = r(d[18]).withRouter(
      r(d[19]).connect(
        function (t, n) {
          return {
            isProcessing: t.contactImport.requestInFlight,
            shouldRender: r(d[15]).shouldRenderContactImportUpsell(
              t,
              i(d[8])(n.variant)
            ),
          };
        },
        function (t, n) {
          var o = n.redirectToContactsPage,
            s = n.variant;
          return {
            onDismissed: function () {
              "CHAINING_LIST_ITEM" === s
                ? t({ type: r(d[16]).CI_CHAINING_LIST_UPSELL_DISMISSED })
                : "EMPTY_FEED_CAROUSEL_CARD" === s &&
                  t({ type: r(d[16]).CI_EMPTY_FEED_CAROUSEL_UPSELL_DISMISSED });
            },
            onImportContacts: function () {
              t(
                r(d[17]).importContacts({
                  redirectToContactsPage: void 0 === o || o,
                })
              );
            },
          };
        }
      )(p)
    );
    (e.default = u),
      (e.IMPORT_CONTACTS_LEGAL_DISCLAIMER = T),
      (e.LegalDisclaimer = _);
  },
  10289247,
  [
    9895940,
    9764899,
    3,
    9895962,
    10158154,
    10158338,
    9895953,
    9764914,
    9895943,
    10289253,
    10158213,
    10289254,
    10289255,
    10289256,
    10289257,
    10289242,
    10289258,
    10289259,
    6,
    5,
  ]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var t = {
        AVATAR: { HEIGHT: 88, WIDTH: 88 },
        CARD: { HEIGHT: 344, WIDTH: 236 },
        IMAGE: { HEIGHT: 74, WIDTH: 74 },
      },
      n = function (n) {
        var l = n.children,
          o = n.dangerouslySetClassName,
          c = n.onClick;
        return a(d[1]).createElement(
          "div",
          {
            className: null === o || void 0 === o ? void 0 : o.__className,
            onClick: c,
            role: "link",
            tabIndex: "0",
          },
          a(d[1]).createElement(
            r(d[2]).Box,
            {
              alignItems: "center",
              color: "ig-primary-background",
              dangerouslySetClassName: { __className: "R-Yxq" },
              flex: "grow",
              height: t.CARD.HEIGHT,
              padding: 1,
              width: t.CARD.WIDTH,
            },
            l
          )
        );
      },
      l = i(d[3])(function (l) {
        var o = l.body,
          c = l.button,
          s = l.dangerouslySetClassName,
          u = l.header,
          E = l.icon,
          I = l.onDismiss;
        return a(d[1]).createElement(
          n,
          { dangerouslySetClassName: s },
          a(d[1]).createElement(
            r(d[2]).Box,
            {
              alignItems: "center",
              dangerouslySetClassName: { __className: "_6d4V5" },
              height: t.AVATAR.HEIGHT,
              justifyContent: "center",
              marginTop: 11,
              shape: "circle",
              width: t.AVATAR.WIDTH,
            },
            E
          ),
          a(d[1]).createElement(
            r(d[2]).Box,
            { padding: 3 },
            a(d[1]).createElement(
              r(d[2]).Text.Headline2,
              { textAlign: "center" },
              u
            )
          ),
          I &&
            a(d[1]).createElement(
              r(d[2]).Box,
              { position: "absolute", right: !0 },
              a(d[1]).createElement(r(d[2]).IconButton, {
                alt: r(d[4])(2607),
                icon: r(d[2]).ICONS.GREY_CLOSE,
                onClick: I,
              })
            ),
          a(d[1]).createElement(
            r(d[2]).Box,
            { flex: "grow", paddingX: 3 },
            a(d[1]).createElement(
              r(d[2]).Text.Body,
              { color: "ig-secondary-text", textAlign: "center" },
              o
            )
          ),
          a(d[1]).createElement(r(d[2]).Box, { marginBottom: 5 }, c)
        );
      }),
      o = i(d[3])(n);
    (e.default = o), (e.SIZES = t), (e.UpsellCard = l);
  },
  10289256,
  [10289262, 3, 9895962, 10289263, 9895940]
);
__d(function () {}, 10289262, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    function t() {
      r(d[0]).openURL(r(d[1]).CONTACT_IMPORT_DATA_POLICY_PATH);
    }
    function o() {
      return i(d[2])().pixelRatio >= 1.5
        ? "/static/images/ci/contacts-facepile-2x.jpg/ca81c1e43461.jpg 2x"
        : "/static/images/ci/contacts-facepile-1x.jpg/df9b3f3bde41.jpg";
    }
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = function (n) {
      return a(d[3]).createElement(
        r(d[4]).Dialog,
        {
          body: r(d[5])(3128),
          media:
            !n.hideIcon &&
            a(d[3]).createElement(
              r(d[4]).Box,
              { alignItems: "center", justifyContent: "center", width: "100%" },
              a(d[3]).createElement("img", { alt: r(d[5])(3687), srcSet: o() })
            ),
          onModalClose: n.onClose,
          title: r(d[5])(1083),
        },
        n.onConfirm &&
          a(d[3]).createElement(
            r(d[4]).DialogItem,
            { color: "ig-primary-button", onClick: n.onConfirm },
            r(d[6]).GET_STARTED
          ),
        a(d[3]).createElement(
          r(d[4]).DialogItem,
          {
            color: n.onConfirm ? "ig-secondary-button" : "ig-primary-button",
            onClick: t,
          },
          r(d[6]).LEARN_MORE
        ),
        a(d[3]).createElement(
          r(d[4]).DialogItem,
          { onClick: n.onClose },
          r(d[6]).CLOSE_TEXT
        )
      );
    };
    n.defaultProps = { hideIcon: !0 };
    var c = n;
    e.default = c;
  },
  10289257,
  [10158225, 10158338, 10158239, 3, 9895962, 9895940, 9895953]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }),
      (e.default = function () {
        var t = r(d[0]).useState(r(d[1]).fetchWindowOrientation()),
          n = i(d[2])(t, 2),
          o = n[0],
          u = n[1],
          w = r(d[0]).useState(window.devicePixelRatio),
          c = i(d[2])(w, 2),
          f = c[0],
          s = c[1],
          l = r(d[0]).useState(window.innerHeight),
          v = i(d[2])(l, 2),
          h = v[0],
          p = v[1],
          W = r(d[0]).useState(window.innerWidth),
          x = i(d[2])(W, 2),
          P = x[0],
          R = x[1];
        return (
          r(d[0]).useEffect(function () {
            var t = function () {
                u(r(d[1]).fetchWindowOrientation),
                  s(window.devicePixelRatio),
                  p(window.innerHeight),
                  R(window.innerWidth);
              },
              n = !1,
              o = null;
            if (r(d[4]).isDesktop()) {
              var w = function () {
                s(window.devicePixelRatio), (o = setTimeout(w, 1e3));
              };
              w();
            }
            var c = i(d[5]).add(window, "resize", function () {
              n ||
                ((n = !0),
                r(d[3]).measure(function () {
                  try {
                    t();
                  } finally {
                    n = !1;
                  }
                }));
            });
            return function () {
              r(d[4]).isDesktop() && clearTimeout(o), c.remove();
            };
          }, []),
          { orientation: o, pixelRatio: f, viewportHeight: h, viewportWidth: P }
        );
      });
  },
  10158239,
  [3, 10158244, 69, 10158176, 9764909, 10158128]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]), r(d[1]);
    e.default = function (t) {
      var l = t.className,
        n = t.errorText,
        c = t.onRetry;
      i(d[2])(t, ["className", "errorText", "onRetry"]);
      return a(d[3]).createElement(
        "div",
        { className: i(d[4])(l, "TqMen") },
        a(d[3]).createElement(
          "button",
          {
            "aria-label": r(d[5]).RETRY_TEXT,
            className: "_1n6a3",
            onClick: c,
            tabIndex: "0",
          },
          a(d[3]).createElement("div", { className: "mEFkC coreSpriteReload" }),
          a(d[3]).createElement(
            "div",
            { className: "JMO_o" },
            n || r(d[5]).FAILED_TO_LOAD_TEXT
          )
        )
      );
    };
  },
  12386336,
  [9895938, 12386347, 9764901, 3, 9895958, 9895953]
);
__d(function () {}, 12386347, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]), r(d[1]);
    var t = function (t) {
      return a(d[2]).createElement(
        i(d[3]),
        {
          className: "HUW1v hUQXy",
          href: t.href,
          onClick: t.onClick,
          params: t.params,
        },
        r(d[4])(1089)
      );
    };
    e.default = t;
  },
  10289244,
  [9895937, 10289251, 3, 9895944, 9895940]
);
__d(function () {}, 10289251, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    function s(s) {
      return !s.suggestedUsers.viewerHasFBConnect;
    }
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0]).createSelector(
        s,
        r(d[1]).isFBConnectEligible,
        function (s, t) {
          return (
            !s &&
            t &&
            !1 !== i(d[2])._("125", "0") &&
            !1 !== i(d[2])._("127", "2")
          );
        }
      ),
      n = r(d[0]).createSelector(
        function (s) {
          return s.suggestedUsers.ids;
        },
        function (s) {
          return s.suggestedUsers.dismissedAysfIds;
        },
        function (s, t) {
          return s.subtract(t).toArray();
        }
      ),
      u = r(d[0]).createSelector(
        function (s) {
          return s.suggestedUsers.dismissedAysfIds;
        },
        function (s, t) {
          return i(d[3])(t.userIds).map(function (t) {
            return r(d[4]).getUserById(s, t);
          });
        },
        function (s, t) {
          return t
            .filter(function (t) {
              return !s.has(t.id);
            })
            .toArray();
        }
      ),
      o = r(d[0]).createSelector(
        function (s) {
          return s.suggestedUsers.ids;
        },
        function (s) {
          return s.toArray();
        }
      );
    (e.isViewerFacebookConnected = s),
      (e.shouldDisplayFacebookConnect = t),
      (e.getNonDismissedAysfIds = n),
      (e.getProfileChainingFailure = function (s, t) {
        return !!s.suggestedUsers.profileChainingFailures.get(t);
      }),
      (e.getProfileChainingSuggestions = function (s, t) {
        return s.suggestedUsers.profileChainingSuggestions.get(t);
      }),
      (e.getFeedAysfUsers = u),
      (e.getSuggestions = o),
      (e.isInitialLoad = function (s) {
        return (
          s.suggestedUsers.isLoadingSuggestions &&
          0 === s.suggestedUsers.ids.size
        );
      });
  },
  10289241,
  [9, 10289248, 9895961, 9895943, 9895966]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }),
      (e.isFBConnectEligible = function (n) {
        return n.fb.status !== r(d[0]).STATUS.ineligible;
      }),
      (e.isConnected = function (n) {
        return n.fb.status === r(d[0]).STATUS.connected;
      });
  },
  10289248,
  [10289249]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var t = function (t) {
      return a(d[1]).createElement(
        "section",
        { className: i(d[2])("ABCxa", t.className) },
        a(d[1]).createElement(
          "div",
          { className: "JErX0" },
          a(d[1]).createElement("div", { className: "ig3mj" }, t.icon),
          a(d[1]).createElement("div", { className: "olLwo" }, t.headerText),
          a(d[1]).createElement("div", { className: "f5C5x" }, t.bodyText),
          !t.hideAction &&
            a(d[1]).createElement(
              r(d[3]).Button,
              {
                disabled: t.buttonDisabled,
                loading: t.isProcessing,
                onClick: t.onButtonClick,
              },
              t.buttonText
            ),
          t.footer
        )
      );
    };
    t.defaultProps = { hideAction: !1 };
    var n = t;
    e.default = n;
  },
  10289254,
  [10289260, 3, 9895958, 9895962]
);
__d(function () {}, 10289260, []);
