__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }),
      r(d[0]),
      (e.default = function (l) {
        var o = l.followType,
          t = l.onClose;
        return a(d[1]).createElement(
          r(d[2]).Modal,
          { dangerouslySetClassName: { __className: "HYpXt" }, onClose: t },
          a(d[1]).createElement(
            r(d[2]).ModalHeader,
            { onClose: t },
            r(d[3]).getFollowListHeader(o)
          ),
          a(d[1]).createElement(i(d[4]), { followType: o })
        );
      }),
      (e.PAGE_ID = i(d[5]).followList);
  },
  13434880,
  [13434881, 3, 9895962, 13434882, 13434883, 9895951]
);
__d(function () {}, 13434881, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0])(3538),
      n = r(d[0])(9);
    e.getFollowListHeader = function (o) {
      return "inbound" === o ? t : n;
    };
  },
  13434882,
  [9895940]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = (function (t) {
      function n() {
        for (var n, o = arguments.length, l = new Array(o), u = 0; u < o; u++)
          l[u] = arguments[u];
        return (
          (n = t.call.apply(t, [this].concat(l)) || this),
          (n.$FollowListContent1 = r(d[1]).passesServerChecks(
            r(d[1]).SERVER_CHECK_KEYS.HASHTAG_FOLLOW_ENABLE
          )),
          n
        );
      }
      i(d[0])(n, t);
      return (
        (n.prototype.render = function () {
          return "outbound" === this.props.followType &&
            this.$FollowListContent1
            ? a(d[2]).createElement(i(d[3]), null)
            : a(d[2]).createElement(i(d[4]), null);
        }),
        n
      );
    })(a(d[2]).Component);
    e.default = t;
  },
  13434883,
  [9764914, 9764880, 3, 13434884, 13434885]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0])(355),
      n = r(d[0])(2503),
      o = (function (o) {
        function u() {
          return o.apply(this, arguments) || this;
        }
        i(d[1])(u, o);
        return (
          (u.prototype.render = function () {
            var o = i(d[2])(this.props.match.params.username);
            return a(d[3]).createElement(
              r(d[4]).Tabs,
              null,
              a(d[3]).createElement(
                r(d[4]).Tab,
                { component: i(d[5]), path: r(d[6]).buildUserFollowingLink(o) },
                t
              ),
              a(d[3]).createElement(
                r(d[4]).Tab,
                {
                  component: i(d[7]),
                  path: r(d[6]).buildUserHashtagFollowingLink(o),
                },
                n
              )
            );
          }),
          u
        );
      })(a(d[3]).Component),
      u = r(d[8]).withRouter(o);
    e.default = u;
  },
  13434884,
  [9895940, 9764914, 9895943, 3, 9895962, 13434885, 9895959, 13434886, 6]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    function t(t) {
      var o = r(d[19]).matchPath(t, { path: "/:username/:type/:viewType?/" });
      return null === o || void 0 === o ? void 0 : o.params;
    }
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var o = { x: 1, y: 2 },
      s = 4,
      n = (function (t) {
        function n() {
          for (var o, n = arguments.length, l = new Array(n), u = 0; u < n; u++)
            l[u] = arguments[u];
          return (
            (o = t.call.apply(t, [this].concat(l)) || this),
            (o.$UserFollowListContent1 = !1),
            (o.$UserFollowListContent5 = function () {
              o.$UserFollowListContent4() &&
                o.props.requestNextFollowListPage(
                  o.props.userId,
                  o.props.followType
                );
            }),
            (o.$UserFollowListContent7 = function () {
              var t = o.props.viewType;
              if ("mutualOnly" === t) return o.props.mutualUsers.slice(0, s);
              if ("mutualFirst" === t) {
                var n = o.props.users.filter(function (t) {
                  var o;
                  return (
                    (null === (o = t.relationship) || void 0 === o
                      ? void 0
                      : o.followedByViewer.state) !==
                    r(d[2]).FOLLOW_STATUS_FOLLOWING
                  );
                });
                return [].concat(i(d[3])(o.props.mutualUsers), i(d[3])(n));
              }
              return o.props.users;
            }),
            o
          );
        }
        i(d[1])(n, t);
        var l = n.prototype;
        return (
          (l.componentDidMount = function () {
            (this.$UserFollowListContent1 = this.$UserFollowListContent2()),
              r(d[4]).logPageView(i(d[5]).followList, {
                followType: this.props.followType,
              });
          }),
          (l.componentDidUpdate = function (t) {
            this.$UserFollowListContent3 &&
              this.$UserFollowListContent4() &&
              t.users !== this.props.users &&
              this.$UserFollowListContent3.forceRecompute();
          }),
          (l.$UserFollowListContent2 = function () {
            return (
              i(d[6])._("222") &&
              "inbound" === this.props.followType &&
              this.props.viewerId === this.props.userId
            );
          }),
          (l.$UserFollowListContent4 = function () {
            return (
              "mutualOnly" !== this.props.viewType &&
              this.props.hasMore &&
              !this.props.isLoading
            );
          }),
          (l.$UserFollowListContent6 = function (t, o, s) {
            var n = !!s;
            if (t)
              return r(d[7]).CONNECTIONS_CONTAINER_MODULES
                .profile_social_context;
            switch (o) {
              case "inbound":
                return n
                  ? r(d[7]).CONNECTIONS_CONTAINER_MODULES.self_followers
                  : r(d[7]).CONNECTIONS_CONTAINER_MODULES.followers;
              case "outbound":
                return n
                  ? r(d[7]).CONNECTIONS_CONTAINER_MODULES.self_following
                  : r(d[7]).CONNECTIONS_CONTAINER_MODULES.following;
            }
            return r(d[7]).CONNECTIONS_CONTAINER_MODULES.followers;
          }),
          (l.render = function () {
            var t = this,
              s = this.props,
              n = s.canSeeFollowList,
              l = s.followType,
              u = s.hasMore,
              p = s.hasMoreMutuals,
              c = s.isLoading,
              w = s.modal,
              f = s.mutualUsers,
              h = s.users,
              L = s.viewType,
              C = s.viewerId,
              N = "mutualOnly" === L,
              U = this.$UserFollowListContent6(N, l, C),
              v = N ? p : u;
            if (0 === (N ? f : h).length)
              return v
                ? a(d[8]).createElement(
                    i(d[10]),
                    { className: w ? "isgrP" : "" },
                    i(d[11])(10).map(function (t) {
                      return a(d[8]).createElement(
                        r(d[12]).ListItemPlaceholder,
                        { key: t }
                      );
                    })
                  )
                : a(d[8]).createElement(i(d[9]), {
                    containerModule: U,
                    followType: l,
                  });
            var y = h.length <= 12 || N,
              O = r(d[13]).isDesktop() ? i(d[10]) : "div";
            return a(d[8]).createElement(
              O,
              { className: w ? "isgrP" : "" },
              a(d[8]).createElement(i(d[14]), {
                analyticsContext: U,
                borderlessFollowButton: this.$UserFollowListContent1,
                canShowRemoveButton: this.$UserFollowListContent1,
                className: (w ? "jSC57" : "") + " " + (w ? "" : "jjbaz"),
                hasStoryRings: !0,
                isLoading: c,
                items: this.$UserFollowListContent7(),
                useCoreListComponent: y,
                viewerId: i(d[15])(C),
              }),
              N &&
                !c &&
                n &&
                a(d[8]).createElement(
                  "div",
                  { className: "SfPzb" },
                  a(d[8]).createElement(
                    r(d[12]).Button,
                    {
                      borderless: !0,
                      href:
                        "/" +
                        i(d[15])(this.props.username) +
                        "/followers/mutualFirst",
                    },
                    r(d[16])(45)
                  )
                ),
              this.$UserFollowListContent4() &&
                a(d[8]).createElement(i(d[17]), {
                  boundScaleFactor: o,
                  className: w ? "oMwYe" : "",
                  onScrollEnter: this.$UserFollowListContent5,
                  ref: function (o) {
                    return (t.$UserFollowListContent3 = o);
                  },
                }),
              y &&
                !u &&
                a(d[8]).createElement(i(d[18]), {
                  analyticsContext: U,
                  viewModule: r(d[7]).VIEW_MODULES.follower_list,
                })
            );
          }),
          n
        );
      })(a(d[8]).Component),
      l = r(d[19]).withRouter(
        r(d[26]).connect(
          function (o, s) {
            var n = s.match,
              l = n.params;
            null == l.username && (l = i(d[15])(t(n.path)));
            var u = "following" === i(d[15])(l.type) ? "outbound" : "inbound",
              p = i(d[15])(l.username),
              c = r(d[20]).getViewer(o),
              w = i(d[15])(r(d[20]).getUserByUsername(o, p)),
              f = w.id,
              h = o.followLists.get(f, r(d[21]).EMPTY_LISTS)[u],
              L = o.followLists.get(f, r(d[21]).EMPTY_LISTS)[u + "Mutual"],
              C = o.relationships;
            return {
              canSeeFollowList: r(d[22]).canViewerSeeFollowList(C, c, w),
              followType: u,
              isLoading: r(d[23]).isFetching(h.pagination),
              hasMore: !1 !== r(d[23]).hasNextPage(h.pagination),
              hasMoreMutuals: !1 !== r(d[23]).hasNextPage(L.pagination),
              modal: r(d[24]).shouldSpawnModals(
                o.displayProperties.viewportWidth
              ),
              mutualUsers: L.userIds.toSeq().map(function (t) {
                return {
                  user: r(d[20]).getUserById(o, t),
                  relationship: r(d[22]).getRelationship(C, t),
                };
              }),
              userId: f,
              username: p,
              users: h.userIds
                .toSeq()
                .slice(0, r(d[23]).getVisibleCount(h.pagination))
                .map(function (t) {
                  return {
                    user: r(d[20]).getUserById(o, t),
                    relationship: r(d[22]).getRelationship(C, t),
                  };
                })
                .toArray(),
              viewType: l.viewType,
              viewerId: null === c || void 0 === c ? void 0 : c.id,
            };
          },
          function (t) {
            return {
              requestNextFollowListPage: function (o, s) {
                return t(r(d[25]).requestNextFollowListPage(o, s));
              },
            };
          }
        )(n)
      );
    e.default = l;
  },
  13434885,
  [
    13434887,
    9764914,
    10158089,
    9764896,
    9764900,
    9895951,
    9764899,
    10158213,
    3,
    13434888,
    13434889,
    10158332,
    9895962,
    9764909,
    13434890,
    9895943,
    9895940,
    12517379,
    10289195,
    6,
    9895966,
    13434891,
    10158088,
    10158372,
    10158276,
    13434892,
    5,
  ]
);
__d(function () {}, 13434887, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = { inbound: r(d[0])(2612), outbound: r(d[0])(3157) },
      n = { inbound: r(d[0])(1649), outbound: r(d[0])(660) };
    e.default = function (o) {
      var l = o.containerModule,
        u = o.followType,
        c = a(d[1]).createElement(i(d[2]), {
          analyticsContext: l,
          viewModule: r(d[3]).VIEW_MODULES.follower_list,
        });
      return a(d[1]).createElement(i(d[4]), {
        icon: a(d[1]).createElement(r(d[5]).Icon, {
          alt: t[u],
          icon: r(d[5]).ICONS.ADD_FRIEND_OUTLINE_96,
        }),
        subtitle: n[u],
        suggestedContent: c,
        title: t[u],
      });
    };
  },
  13434888,
  [9895940, 3, 10289195, 10158213, 13434893, 9895962]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = r(d[0])(1553),
      s = function () {
        return a(d[1]).createElement(
          r(d[2]).Box,
          { paddingX: 4, paddingY: 3 },
          a(d[1]).createElement(
            r(d[2]).Button,
            { borderless: !0, href: r(d[3]).DISCOVER_PEOPLE_PATH },
            r(d[0])(2800)
          )
        );
      },
      n = i(d[8])("FetchingSuggestedUserList", function (n) {
        var o = n.analyticsContext,
          l = n.avatarSize,
          u = void 0 === l ? "medium" : l,
          c = n.backgroundColor,
          E = n.borderlessFollowButton,
          U = void 0 !== E && E,
          S = n.count,
          _ = n.footer,
          v = n.header,
          T = n.hideName,
          C = void 0 !== T && T,
          L = n.hideUpsells,
          f = void 0 !== L && L,
          h = n.initialRenderCount,
          D = void 0 === h ? r(d[4]).SUL_FETCH_SUGGESTED_COUNT_DEFAULT : h,
          F = n.onDisplayDone,
          b = n.variant,
          p = void 0 === b ? "LIST" : b,
          N = n.viewModule,
          A = r(d[5]).useSelector(
            a(d[1]).useCallback(function (t) {
              return {
                isLoading: t.suggestedUsers.isLoadingSuggestions,
                suggestedUserIds: t.suggestedUsers.ids.toArray(),
              };
            }, []),
            r(d[5]).shallowEqual
          ),
          G = A.isLoading,
          H = A.suggestedUserIds,
          I = r(d[5]).useDispatch(),
          O = a(d[1]).useCallback(
            function (t) {
              return r(d[6]).hasSuggestedUsersV2()
                ? I(r(d[4]).loadSULV2())
                : I(r(d[4]).loadSUL({ suggestedCount: t }));
            },
            [I]
          );
        return (
          a(d[1]).useEffect(
            function () {
              0 === H.length && O(r(d[4]).SUL_FETCH_SUGGESTED_COUNT_DEFAULT);
            },
            [O, H.length]
          ),
          a(d[1]).useEffect(
            function () {
              H.length > 0 && F();
            },
            [F, H]
          ),
          a(d[1]).createElement(
            a(d[1]).Fragment,
            null,
            a(d[1]).createElement(i(d[7]), {
              analyticsContext: o,
              avatarSize: u,
              backgroundColor: c,
              borderlessFollowButton: U,
              hideName: C,
              hideUpsells: f,
              initialRenderCount: D,
              isLoading: G,
              subHeader: void 0 !== v ? v : t,
              userIds: isNaN(S)
                ? H.slice(0, r(d[4]).SUL_FETCH_SUGGESTED_COUNT_DEFAULT)
                : H.slice(0, S),
              variant: p,
              viewModule: N,
            }),
            "LIST" === p && (void 0 !== _ ? _ : a(d[1]).createElement(s, null))
          )
        );
      });
    (e.default = n), (e.HEADER_TEXT = t);
  },
  10289195,
  [9895940, 3, 9895962, 10158338, 10158367, 5, 10289238, 10289239, 10289240]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }),
      (e.hasSuggestedUsersV2 = function (t) {
        return i(d[0])._("155", "0", t);
      });
  },
  10289238,
  [9895961]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = function (n) {
      var o = n.analyticsContext,
        t = n.avatarSize,
        l = void 0 === t ? "large" : t,
        s = n.borderlessFollowButton,
        c = void 0 !== s && s,
        u = n.backgroundColor,
        v = void 0 === u ? "ig-primary-background" : u,
        C = (n.children, n.footer),
        E = n.hideName,
        _ = void 0 !== E && E,
        p = (n.hideStoryRings, n.hideUpsells),
        f = void 0 !== p && p,
        I = n.initialRenderCount,
        T = void 0 === I ? r(d[0]).SUL_FETCH_SUGGESTED_COUNT_DEFAULT : I,
        h = n.isLoading,
        S = n.onDismiss,
        x = n.subHeader,
        y = n.userIds,
        b = n.variant,
        D = void 0 === b ? "LIST" : b,
        F = n.viewModule,
        k = {},
        w = r(d[1]).useSelector(
          a(d[2]).useCallback(function (n) {
            return {
              canFBConnect: r(d[3]).shouldDisplayFacebookConnect(n),
              canImportContacts: r(d[4]).shouldRenderContactImportUpsell(
                n,
                "LIST_ITEM"
              ),
            };
          }, []),
          r(d[1]).shallowEqual
        ),
        B = w.canFBConnect,
        L = w.canImportContacts,
        N = function (n) {
          var o = n.followedByViewer,
            t = n.index,
            l = n.userId;
          o || M("recommended_follow_button_tapped", l, t);
        },
        U = function (n) {
          var o = n.index,
            t = n.userId;
          M("recommended_username_tapped", t, o);
        },
        O = function (n, o) {
          if (null != y)
            for (var t = n; t <= o - 1; ++t) {
              var l = y[t];
              k[l] || (M("recommended_user_impression", l, t), (k[l] = !0));
            }
        },
        M = function (n, t, l) {
          r(d[5]).logConnectionAction({
            eventName: n,
            position: l,
            targetId: t,
            containerModule: o,
            viewModule: F,
          });
        };
      return "GRID" === D
        ? a(d[2]).createElement(i(d[6]), {
            avatarSize: l,
            isLoading: h,
            onFollowClick: N,
            onUsernameClick: U,
            onVisibilityChange: O,
            subHeader: x,
            suffix: a(d[2]).createElement(i(d[7]), {
              href: r(d[8]).DISCOVER_PEOPLE_PATH,
            }),
            userIds: y || [],
          })
        : a(d[2]).createElement(
            a(d[2]).Fragment,
            null,
            null != x &&
              a(d[2]).createElement(
                r(d[9]).Box,
                { marginBottom: 3, marginTop: 4, paddingX: 3 },
                a(d[2]).createElement(r(d[9]).Text.Section, null, x)
              ),
            a(d[2]).createElement(
              r(d[9]).Box,
              { color: v, paddingY: 2 },
              !f &&
                a(d[2]).createElement(
                  a(d[2]).Fragment,
                  null,
                  r(d[10]).checkGraphDifferentiationQE() &&
                    a(d[2]).createElement(i(d[11]), {
                      analyticsContext: r(d[5]).CONNECTIONS_CONTAINER_MODULES
                        .discover_people,
                    }),
                  a(d[2]).createElement(i(d[12]), {
                    analyticsContext: o,
                    variant: "LIST_ITEM",
                  }),
                  ((B && r(d[10]).checkGraphDifferentiationQE()) || L) &&
                    a(d[2]).createElement(
                      r(d[9]).Box,
                      { paddingY: 2 },
                      a(d[2]).createElement(r(d[9]).Divider, null)
                    )
                ),
              a(d[2]).createElement(i(d[13]), {
                avatarSize: l,
                avatarTriggerAnalyticsContext: "suggested_user_avatar",
                borderlessFollowButton: c,
                hideName: _,
                hoverPositionType: "fixed",
                initialRenderCount: T,
                isLoading: Boolean(h),
                onDismiss: S,
                onFollowClick: N,
                onScrollChange: function (n) {
                  var o = n.index,
                    t = n.userId;
                  k[t] || (M("recommended_user_impression", t, o), (k[t] = !0));
                },
                onUsernameClick: U,
                userIds: y || [],
                usernameTriggerAnalyticsContext: "suggested_user",
              }),
              C
            )
          );
    };
    e.default = n;
  },
  10289239,
  [
    10158367,
    5,
    3,
    10289241,
    10289242,
    10158213,
    10289243,
    10289244,
    10158338,
    9895962,
    10289245,
    10289246,
    10289247,
    10158266,
  ]
);
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
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = function (n) {
      var t = n.isLoading,
        o = n.onFollowClick,
        l = n.onUsernameClick,
        c = n.onVisibilityChange,
        u = n.subHeader,
        s = n.suffix,
        f = n.userIds,
        k = function (n) {
          o && o(n);
        },
        p = function (n) {
          l && l(n);
        };
      return t
        ? a(d[0]).createElement(
            r(d[1]).Box,
            { alignItems: "center", marginTop: 4, width: "100%" },
            a(d[0]).createElement(r(d[1]).Spinner, null)
          )
        : a(d[0]).createElement(
            r(d[1]).Deck,
            {
              cardType: "USER",
              hasBlur: !0,
              headerText: u,
              onVisibilityChange: function (n, t) {
                c && c(n, t);
              },
              suffix: s,
            },
            f.map(function (n, t) {
              return a(d[0]).createElement(i(d[2]), {
                id: n,
                key: t,
                onFollowClick: k,
                onUsernameClick: p,
                position: t,
              });
            })
          );
    };
    e.default = n;
  },
  10289243,
  [3, 9895962, 10289250]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = function (n) {
      var l = n.analyticsContext,
        t = n.id,
        s = n.onFollowClick,
        o = n.position,
        u = r(d[0]).useSelector(
          a(d[1]).useCallback(
            function (l) {
              return {
                relationship: r(d[2]).getRelationship(l.relationships, n.id),
                user: r(d[3]).getUserById(l, n.id),
              };
            },
            [n.id]
          ),
          r(d[0]).shallowEqual
        ),
        c = u.relationship,
        f = u.user,
        p = f.profilePictureUrl,
        C = f.suggestionDescription,
        h = f.username;
      return null == p || null == C || null == h
        ? null
        : a(d[1]).createElement(r(d[4]).UserCard, {
            button: a(d[1]).createElement(i(d[5]), {
              analyticsContext: l,
              onClick: function () {
                null != s &&
                  c &&
                  s({
                    index: o,
                    userId: t,
                    followedByViewer: r(d[2]).followedByViewer(c),
                  });
              },
              relationship: c,
              userId: f.id,
            }),
            isVerified: f.isVerified,
            onUsernameClick: function () {
              n.onUsernameClick({ index: o, userId: t });
            },
            src: p,
            subtitle: C,
            username: h,
          });
    };
    e.default = n;
  },
  10289250,
  [5, 3, 10158088, 9895966, 9895962, 10158212]
);
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
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = "connect_to_facebook",
      n = r(d[0])(39),
      o = r(d[0])(2319),
      c = r(d[0])(672),
      l = function (l) {
        var u = r(d[1]).useSelector(
            a(d[2]).useCallback(function (t) {
              return {
                canFBConnect: r(d[3]).shouldDisplayFacebookConnect(t),
                isLoading: r(d[3]).isInitialLoad(t),
              };
            }, []),
            r(d[1]).shallowEqual
          ),
          s = u.canFBConnect,
          C = u.isLoading,
          E = a(d[2]).useState(!1),
          _ = i(d[4])(E, 2),
          O = _[0],
          f = _[1],
          B = r(d[5]).parseQueryParams();
        return (
          null != B[t] &&
            B[t].length > 0 &&
            (i(d[6]).replace(i(d[6]).location.pathname), f(!0)),
          O
            ? a(d[2]).createElement(
                r(d[7]).Toast,
                {
                  duration: 1500,
                  onClose: function () {
                    return f(!1);
                  },
                },
                r(d[8]).FACEBOOK_COMPLETED
              )
            : s &&
              a(d[2]).createElement(r(d[7]).ListItem, {
                action: a(d[2]).createElement(
                  r(d[7]).Button,
                  {
                    disabled: C,
                    loading: C,
                    onClick: function () {
                      return r(d[9]).redirectToFBOAuth(
                        i(d[6]).location.pathname + "?" + t + "=true",
                        l.analyticsContext
                      );
                    },
                  },
                  c
                ),
                icon: a(d[2]).createElement(r(d[7]).BorderedIcon, {
                  alt: n,
                  color: "facebook",
                  icon: r(d[7]).ICONS.FACEBOOK_CIRCLE_FILLED_24,
                  size: r(d[7]).CORE_CONSTANTS.AVATAR_SIZES.medium,
                }),
                subtitle: o,
                title: a(d[2]).createElement(
                  r(d[7]).Text.BodyEmphasized,
                  null,
                  n
                ),
                truncateText: !1,
              })
        );
      };
    e.default = l;
  },
  10289246,
  [9895940, 5, 3, 10289241, 69, 10289153, 9895941, 9895962, 10289252, 10289245]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var O = r(d[0])(3087),
      E = r(d[0])(3038),
      _ = r(d[0])(3691),
      T = r(d[0])(96),
      C = r(d[0])(193),
      P = r(d[0])(1627),
      A = r(d[0])(3517),
      D = r(d[0])(1150),
      R = r(d[0])(166),
      H = r(d[0])(1423),
      I = r(d[0])(238),
      F = r(d[0])(298),
      L = r(d[0])(3375),
      B = r(d[0])(3129),
      N = r(d[0])(3272),
      S = r(d[0])(774),
      Y = r(d[0])(1951),
      t = r(d[0])(2369),
      M = r(d[0])(3449),
      u = r(d[0])(1639),
      K = r(d[0])(3421),
      c = r(d[0])(3386),
      n = r(d[0])(1234);
    (e.GETTING_STARTED = O),
      (e.FIRST_PHOTO_HEADER = E),
      (e.FIRST_PHOTO_BODY = _),
      (e.FIRST_PHOTO_CTA = T),
      (e.FACEBOOK_BODY = C),
      (e.FACEBOOK_COMPLETED = P),
      (e.FACEBOOK_CTA = A),
      (e.FACEBOOK_HEADER = D),
      (e.CONTACTS_BODY = R),
      (e.CONTACTS_CTA = H),
      (e.CONTACTS_COMPLETED = I),
      (e.CONTACTS_HEADER = F),
      (e.PROFILE_PHOTO_BODY = L),
      (e.PROFILE_PHOTO_CTA = B),
      (e.PROFILE_PHOTO_HEADER = N),
      (e.PHONE_BODY = S),
      (e.PHONE_COMPLETED = Y),
      (e.PHONE_CTA = t),
      (e.PHONE_HEADER = M),
      (e.EDIT_PROFILE_BODY = u),
      (e.EDIT_PROFILE_COMPLETED = K),
      (e.EDIT_PROFILE_CTA = c),
      (e.EDIT_PROFILE_HEADER = n);
  },
  10289252,
  [9895940]
);
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
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = (function (t) {
      function n() {
        for (var n, o = arguments.length, s = new Array(o), l = 0; l < o; l++)
          s[l] = arguments[l];
        return (
          (n = t.call.apply(t, [this].concat(s)) || this),
          (n.$UserList1 = a(d[1]).createRef()),
          (n.$UserList2 = function (t) {
            var o = n.props.onFollowClick;
            o && o(t);
          }),
          (n.$UserList3 = function (t) {
            var o = t.index,
              s = t.isVisible,
              l = n.props,
              u = l.analyticsContext,
              c = l.avatarSize,
              p = l.avatarTriggerAnalyticsContext,
              h = l.borderlessFollowButton,
              y = l.entryPoint,
              C = l.hideName,
              v = l.hoverPositionType,
              f = l.isLoading,
              L = l.userIds,
              U = l.usernameTriggerAnalyticsContext;
            return 0 === L.length
              ? f
                ? a(d[1]).createElement(r(d[2]).ListItemPlaceholder, {
                    key: o,
                    size: c,
                  })
                : null
              : a(d[1]).createElement(i(d[3]), {
                  analyticsContext: u,
                  avatarSize: c,
                  avatarTriggerAnalyticsContext: p,
                  borderlessFollowButton: h,
                  entryPoint: y,
                  hideFollowButton: n.props.hideFollowButton,
                  hideName: C,
                  hideStoryRings: n.props.hideStoryRings,
                  hoverPositionType: v || "absolute",
                  id: L[o],
                  isVisible: s,
                  key: L[o],
                  onDismiss: n.props.onDismiss,
                  onFollowClick: n.$UserList2,
                  onScrollEnter: n.$UserList4,
                  onUsernameClick: n.$UserList5,
                  position: o,
                  usernameTriggerAnalyticsContext: U,
                });
          }),
          (n.$UserList4 = function (t) {
            var o = n.props.onScrollChange;
            o && o(t);
          }),
          (n.$UserList5 = function (t) {
            var o = n.props.onUsernameClick;
            o && o(t);
          }),
          n
        );
      }
      i(d[0])(n, t);
      var o = n.prototype;
      return (
        (o.componentDidUpdate = function (t) {
          null != this.$UserList1.current &&
            this.props.userIds.length === this.props.initialRenderCount &&
            0 === t.userIds.length &&
            this.$UserList1.current.forceUpdate();
        }),
        (o.render = function () {
          var t = this.props,
            n = t.containerSize,
            o = t.initialRenderCount,
            s = t.isLoading,
            l = t.onScroll,
            u = t.userIds;
          return a(d[1]).createElement(
            a(d[1]).Fragment,
            null,
            a(d[1]).createElement(i(d[4]), {
              containerSize: n,
              estimatedItemSize: 65,
              initialRenderCount: o,
              itemCount: u.length || o,
              onScroll: l,
              ref: this.$UserList1,
              renderer: this.$UserList3,
            }),
            u.length > 0 &&
              s &&
              a(d[1]).createElement(
                r(d[2]).Box,
                { alignItems: "center", marginTop: 4 },
                a(d[1]).createElement(r(d[2]).Spinner, { size: "medium" })
              )
          );
        }),
        n
      );
    })(a(d[1]).PureComponent);
    t.defaultProps = {
      avatarTriggerAnalyticsContext: null,
      borderlessFollowButton: !1,
      containerSize: "auto",
      entryPoint: "unknown",
      hideFollowButton: !1,
      hideName: !1,
      hideStoryRings: !1,
      hoverPositionType: null,
      initialRenderCount: 10,
      isLoading: !1,
      usernameTriggerAnalyticsContext: null,
    };
    var n = t;
    e.default = n;
  },
  10158266,
  [9764914, 3, 9895962, 10158268, 10158269]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var t = function (t) {
        var n = t.onClick,
          l = t.user,
          o = l.isVerified,
          s = l.username;
        return void 0 === s
          ? null
          : a(d[1]).createElement(
              i(d[2]),
              { href: r(d[3]).buildUserLink(s), onClick: n, title: s },
              a(d[1]).createElement(
                r(d[4]).Box,
                { direction: "row" },
                a(d[1]).createElement(
                  r(d[4]).Text.BodyEmphasized,
                  {
                    dangerouslySetClassName: { __className: "rWtOq" },
                    display: "truncated",
                  },
                  a(d[1]).createElement(
                    r(d[4]).Box,
                    { alignItems: "center", direction: "row" },
                    s,
                    !0 === o &&
                      a(d[1]).createElement(
                        r(d[4]).Box,
                        { marginStart: 2 },
                        a(d[1]).createElement(r(d[4]).VerifiedBadge, {
                          size: "small",
                        })
                      )
                  )
                )
              )
            );
      },
      n = r(d[15]).connect(function (t, n) {
        return {
          relationship: r(d[6]).getRelationship(t.relationships, n.id),
          user: r(d[14]).getUserById(t, n.id),
          viewer: r(d[14]).getViewer(t),
        };
      })(function (n) {
        var l,
          o = n.analyticsContext,
          s = n.avatarSize,
          u = void 0 === s ? "medium" : s,
          c = n.avatarTriggerAnalyticsContext,
          E = void 0 === c ? null : c,
          C = n.borderlessFollowButton,
          f = n.entryPoint,
          v = n.hideFollowButton,
          p = n.hideName,
          y = n.hideStoryRings,
          S = n.hoverPositionType,
          x = void 0 === S ? null : S,
          T = n.id,
          I = n.isVisible,
          k = n.onDismiss,
          h = void 0 === k ? null : k,
          w = n.onFollowClick,
          A = n.onScrollEnter,
          B = n.onUsernameClick,
          _ = n.position,
          b = n.relationship,
          N = n.user,
          V = n.usernameTriggerAnalyticsContext,
          O = void 0 === V ? null : V,
          P = n.viewer,
          R = r(d[4]).usePreviousValue(I),
          U = r(d[1]).useState(!0),
          z = i(d[5])(U, 2),
          F = z[0],
          D = z[1],
          L = r(d[1]).useCallback(
            function () {
              w &&
                b &&
                w({
                  index: _,
                  userId: T,
                  followedByViewer: r(d[6]).followedByViewer(b),
                });
            },
            [T, w, _, b]
          ),
          M = r(d[1]).useCallback(
            function () {
              A({ index: _, userId: T });
            },
            [T, A, _]
          ),
          Z = r(d[1]).useCallback(
            function () {
              B({ index: _, userId: T });
            },
            [T, B, _]
          );
        r(d[1]).useEffect(
          function () {
            !0 !== R && I && M();
          },
          [M, I, R]
        );
        var j = !v && (null === P || void 0 === P ? void 0 : P.id) !== N.id,
          q = y
            ? a(d[1]).createElement(i(d[7]), {
                profilePictureUrl: i(d[8])(N.profilePictureUrl),
                size: r(d[4]).CORE_CONSTANTS.AVATAR_SIZES[u],
                username: N.username,
              })
            : a(d[1]).createElement(i(d[9]), {
                profilePictureUrl: i(d[8])(N.profilePictureUrl),
                size: r(d[4]).CORE_CONSTANTS.AVATAR_SIZES[u],
                storyEntrypoint: f,
                username: N.username,
              }),
          G = a(d[1]).createElement(
            a(d[1]).Fragment,
            null,
            a(d[1]).createElement(i(d[10]), {
              analyticsContext: o,
              borderless: C,
              onClick: L,
              relationship: b,
              userId: N.id,
              useSmallText: C,
            }),
            null != h &&
              a(d[1]).createElement(
                r(d[4]).Box,
                { marginStart: 3, right: !0 },
                a(d[1]).createElement(r(d[4]).IconButton, {
                  alt: r(d[11]).DISMISS_TEXT,
                  icon: r(d[4]).ICONS.GREY_CLOSE,
                  noMinSize: !0,
                  onClick: function () {
                    D(!1), h(T);
                  },
                })
              )
          );
        return (
          F &&
          a(d[1]).createElement(r(d[4]).ListItem, {
            action: j ? G : void 0,
            context: N.suggestionDescription,
            icon:
              null != x && null != E
                ? a(d[1]).createElement(
                    i(d[12]),
                    {
                      display: "block",
                      positionType: x,
                      triggerAnalyticsContext: E,
                      userId: N.id,
                    },
                    q
                  )
                : q,
            subtitle: p ? null : N.fullName,
            title:
              null != x && null != O
                ? a(d[1]).createElement(i(d[13]), {
                    color: "ig-primary-text",
                    onClick: Z,
                    positionType: x,
                    triggerAnalyticsContext: O,
                    userId: N.id,
                    username:
                      null !==
                        (l =
                          null === N || void 0 === N ? void 0 : N.username) &&
                      void 0 !== l
                        ? l
                        : "",
                  })
                : a(d[1]).createElement(t, { onClick: Z, user: N }),
            truncateText: !1,
          })
        );
      });
    e.default = n;
  },
  10158268,
  [
    10158270,
    3,
    9895944,
    9895959,
    9895962,
    69,
    10158088,
    9895946,
    9895943,
    10158271,
    10158212,
    9895953,
    10158272,
    10158273,
    9895966,
    5,
  ]
);
__d(function () {}, 10158270, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var t = (function (t) {
      function n() {
        return t.apply(this, arguments) || this;
      }
      i(d[0])(n, t);
      return (
        (n.prototype.render = function () {
          return a(d[1]).createElement(
            r(d[2]).Box,
            { flex: "grow", overflow: "scrollY" },
            a(d[1]).createElement(
              r(d[2]).Box,
              { alignItems: "center", justifyContent: "center", paddingY: 10 },
              this.props.icon,
              a(d[1]).createElement(
                r(d[2]).Box,
                { paddingY: 5 },
                a(d[1]).createElement(
                  r(d[2]).Text.Headline2,
                  null,
                  this.props.title
                )
              ),
              a(d[1]).createElement(
                r(d[2]).Text.Body,
                null,
                this.props.subtitle
              )
            ),
            this.props.suggestedContent
          );
        }),
        n
      );
    })(a(d[1]).Component);
    e.default = t;
  },
  13434893,
  [9764914, 3, 9895962]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var t = r(d[1])(977),
      s = function (t) {
        var s = t.children,
          n = t.className,
          l = t.onScrollChange,
          o = t.useCoreListComponent;
        return (
          l && (s = a(d[2]).createElement(i(d[3]), { onScrollChange: l }, s)),
          a(d[2]).createElement(
            "li",
            { className: i(d[4])(o ? "" : "wo9IH", n) },
            s
          )
        );
      },
      n = 100,
      l = 20,
      o = (function (o) {
        function c(t) {
          var s;
          return (
            (s = o.call(this, t) || this),
            (s.$UserList_DEPRECATED3 = function (t, o) {
              var c = s.$UserList_DEPRECATED4() ? l : n,
                E = s.$UserList_DEPRECATED1[t],
                u = o >= c;
              if (
                ((s.$UserList_DEPRECATED1[t] = u),
                s.$UserList_DEPRECATED1.every(function (t) {
                  return null != t;
                }) && E !== u)
              ) {
                var p = Object.keys(s.$UserList_DEPRECATED1)
                  .filter(function (t) {
                    return s.$UserList_DEPRECATED1[t];
                  })
                  .map(function (t) {
                    return +t;
                  });
                s.props.onVisibilityChange && s.props.onVisibilityChange(p);
              }
            }),
            (s.$UserList_DEPRECATED1 = t.items.map(function (t) {
              return null;
            })),
            (s.$UserList_DEPRECATED2 = new (i(d[6]))(i(d[7])(s))),
            s
          );
        }
        i(d[5])(c, o);
        var E = c.prototype;
        return (
          (E.$UserList_DEPRECATED5 = function (t, s) {
            var n,
              l = this.props,
              o = l.canShowRemoveButton,
              c = l.showFollowButton,
              E = this.props.viewerId !== t.id;
            if (!o) return c && E;
            var u =
              (null === s || void 0 === s
                ? void 0
                : null === (n = s.followedByViewer) || void 0 === n
                ? void 0
                : n.state) === r(d[8]).FOLLOW_STATUS_NOT_FOLLOWING;
            return c && E && u;
          }),
          (E.$UserList_DEPRECATED6 = function (t, n, l, o) {
            var c = t.user,
              E = this.props.viewerId !== c.id,
              u = this.$UserList_DEPRECATED5(c, t.relationship),
              p = this.props.canShowRemoveButton && E,
              h =
                this.props.showDescription && Boolean(c.suggestionDescription),
              D = this.props.hasStoryRings ? i(d[9]) : i(d[10]),
              C = a(d[2]).createElement(
                i(d[11]),
                {
                  display: "block",
                  triggerAnalyticsContext: "follower_list_avatar",
                  userId: c.id,
                },
                a(d[2]).createElement(D, {
                  className: o ? "" : "SAvC5",
                  profilePictureUrl: i(d[12])(c.profilePictureUrl),
                  size: this.props.userAvatarSize,
                  storyEntrypoint: "profile",
                  username: c.username,
                })
              ),
              v = u
                ? a(d[2]).createElement(i(d[13]), {
                    analyticsContext: this.props.analyticsContext,
                    borderless: this.props.borderlessFollowButton,
                    onClick: this.props.onFollowClick
                      ? this.$UserList_DEPRECATED2.bind(
                          this.props.onFollowClick,
                          l
                        )
                      : void 0,
                    relationship: t.relationship,
                    userId: c.id,
                    username: c.username,
                    useSmallText: this.props.borderlessFollowButton,
                    viewerLoggedIn: null != this.props.viewerId,
                  })
                : null,
              L = p
                ? a(d[2]).createElement(i(d[14]), {
                    analyticsContext: this.props.analyticsContext,
                    userId: c.id,
                  })
                : null,
              f = p ? L : v,
              _ =
                p && u
                  ? a(d[2]).createElement(
                      a(d[2]).Fragment,
                      null,
                      a(d[2]).createElement(
                        r(d[15]).Box,
                        { display: "inlineBlock", paddingX: 1 },
                        "·"
                      ),
                      v
                    )
                  : null,
              w = a(d[2]).createElement(
                a(d[2]).Fragment,
                null,
                a(d[2]).createElement(
                  i(d[11]),
                  {
                    display: "inline",
                    triggerAnalyticsContext: "follower_list",
                    userId: c.id,
                  },
                  a(d[2]).createElement(i(d[16]), {
                    className: "_0imsa " + (h ? "dwUw5" : ""),
                    onClick: this.props.onUsernameClick
                      ? this.$UserList_DEPRECATED2.bind(
                          this.props.onUsernameClick,
                          l
                        )
                      : null,
                    username: i(d[12])(c.username),
                  })
                ),
                c.isVerified
                  ? a(d[2]).createElement(
                      r(d[15]).Box,
                      { marginStart: 2 },
                      a(d[2]).createElement(r(d[15]).VerifiedBadge, null)
                    )
                  : null
              );
            return a(d[2]).createElement(
              s,
              {
                key: c.username,
                onScrollChange: this.props.onVisibilityChange
                  ? this.$UserList_DEPRECATED2.bind(
                      this.$UserList_DEPRECATED3,
                      l
                    )
                  : null,
                useCoreListComponent: o,
              },
              o
                ? a(d[2]).createElement(r(d[15]).ListItem, {
                    action: f,
                    context: h ? c.suggestionDescription : "",
                    icon: C,
                    subtitle: this.props.hideName ? null : c.fullName,
                    title: a(d[2]).createElement(
                      r(d[15]).Box,
                      { direction: "row" },
                      w,
                      " ",
                      _
                    ),
                  })
                : a(d[2]).createElement(
                    a(d[2]).Fragment,
                    null,
                    a(d[2]).createElement(
                      "div",
                      { className: "uu6c_" },
                      a(d[2]).createElement(
                        "div",
                        { className: "t2ksc" },
                        C,
                        a(d[2]).createElement(
                          "div",
                          { className: "enpQJ" },
                          a(d[2]).createElement(
                            "div",
                            { className: "d7ByH" },
                            w,
                            " ",
                            _
                          ),
                          a(d[2]).createElement(
                            "div",
                            { className: "wFPL8 " + (h ? "r-wGq" : "") },
                            c.fullName
                          )
                        )
                      ),
                      a(d[2]).createElement("div", { className: "Pkbci" }, f)
                    ),
                    h &&
                      a(d[2]).createElement(
                        "div",
                        { className: "YbwEJ" },
                        c.suggestionDescription
                      ),
                    n && this.$UserList_DEPRECATED7(c, t.media)
                  )
            );
          }),
          (E.$UserList_DEPRECATED7 = function (s, n) {
            var l,
              o = this;
            if (n && n.length > 0) {
              var c = n;
              for (
                l = (c = c.slice(0, 3)).map(function (t) {
                  return o.$UserList_DEPRECATED8(t);
                });
                l.length < 3;

              )
                l.push(
                  this.$UserList_DEPRECATED8({
                    code: "@" + String(l.length),
                    id: "",
                    thumbnailSrc: "",
                  })
                );
            } else
              l = s.isPrivate
                ? a(d[2]).createElement(
                    "h3",
                    { className: "vT82g" },
                    r(d[1])(3153)
                  )
                : a(d[2]).createElement("h3", { className: "vT82g" }, t);
            return a(d[2]).createElement("div", { className: "LLzSb" }, l);
          }),
          (E.$UserList_DEPRECATED8 = function (t) {
            return a(d[2]).createElement(
              "div",
              { className: "me823", key: "p" + t.code },
              t.thumbnailSrc &&
                a(d[2]).createElement(i(d[17]), {
                  className: "yHeRa",
                  rich: !0,
                  src: t.thumbnailSrc,
                })
            );
          }),
          (E.$UserList_DEPRECATED4 = function () {
            return (
              this.props.showPreview &&
              this.props.items.some(function (t) {
                return t.media && t.media.length > 0;
              })
            );
          }),
          (E.render = function () {
            var t = this,
              n = this.$UserList_DEPRECATED4(),
              l = this.props,
              o = l.className,
              c = l.isLoading,
              E = l.items,
              u = l.subHeader,
              p = l.useCoreListComponent,
              h = !!c && 0 === E.length;
            return a(d[2]).createElement(
              "ul",
              { className: i(d[4])(o, "_6xe7A") },
              u &&
                !c &&
                (p
                  ? a(d[2]).createElement(
                      r(d[15]).Box,
                      { paddingX: 4, paddingY: 4 },
                      a(d[2]).createElement(r(d[15]).Text.Section, null, u)
                    )
                  : a(d[2]).createElement(
                      s,
                      { className: "_1Yr2-" },
                      a(d[2]).createElement(i(d[18]), null, u)
                    )),
              a(d[2]).createElement(
                "div",
                { className: c ? "" : "PZuss" },
                E.map(function (s, l) {
                  return t.$UserList_DEPRECATED6(s, n, l, p);
                }),
                !!c &&
                  a(d[2]).createElement(
                    s,
                    { className: "QN7kB " + (h ? "A6qiW" : "") },
                    a(d[2]).createElement(i(d[19]), {
                      component: "UserList",
                      position: "absolute",
                      size: "medium",
                      timingEvent: "loadList",
                    })
                  ),
                !!this.props.footer &&
                  a(d[2]).createElement(s, null, this.props.footer)
              )
            );
          }),
          c
        );
      })(a(d[2]).Component);
    o.defaultProps = {
      borderlessFollowButton: !1,
      canShowRemoveButton: !1,
      hasStoryRings: !1,
      hideName: !1,
      showDescription: !1,
      showFollowButton: !0,
      showPreview: !0,
      useCoreListComponent: !1,
    };
    var c = o;
    (e.default = c), (e.UserListItem = s);
  },
  13434890,
  [
    13434894,
    9895940,
    3,
    12517379,
    9895958,
    9764914,
    10092557,
    10092558,
    10158089,
    10158271,
    9895946,
    10158272,
    9895943,
    10158212,
    13434895,
    9895962,
    9895947,
    10289231,
    10748049,
    10289183,
  ]
);
__d(function () {}, 13434894, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    function t(t) {
      var l = t.onCancel,
        c = t.onConfirm,
        u = t.userId,
        s = r(d[1]).useSelector(function (t) {
          return r(d[2]).getUserById(t, u);
        }),
        f = s.profilePictureUrl,
        C = s.username,
        E = r(d[0])(602, { "Username of current profile": C }),
        I = a(d[3]).createElement(r(d[4]).DialogCircleMedia, {
          icon: a(d[3]).createElement(i(d[5]), {
            isLink: !0,
            profilePictureUrl: f,
            size: r(d[6]).SIZES.AVATAR.HEIGHT,
            username: C,
          }),
        });
      return a(d[3]).createElement(
        r(d[4]).Dialog,
        { body: E, media: I, onModalClose: l, title: n },
        a(d[3]).createElement(
          r(d[4]).DialogItem,
          { color: "ig-error-or-destructive", onClick: c },
          o
        ),
        a(d[3]).createElement(
          r(d[4]).DialogItem,
          { onClick: l },
          r(d[7]).CANCEL_TEXT
        )
      );
    }
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = r(d[0])(2113),
      o = r(d[0])(2406),
      l = r(d[0])(1016);
    e.default = function (n) {
      var c = n.analyticsContext,
        u = n.analyticsExtra,
        s = void 0 === u ? {} : u,
        f = n.userId,
        C = r(d[1]).useSelector(function (t) {
          return r(d[8]).getRelationship(t.relationships, f);
        }),
        E = r(d[9]).useState(!1),
        I = i(d[10])(E, 2),
        b = I[0],
        _ = I[1],
        k = r(d[1]).useDispatch(),
        p = r(d[9]).useCallback(
          function () {
            _(!0);
          },
          [_]
        ),
        v = r(d[9]).useCallback(
          function () {
            k(r(d[11]).removeFollower(f, c, s)), _(!1);
          },
          [c, s, k, _, f]
        ),
        S = r(d[9]).useCallback(
          function () {
            return _(!1);
          },
          [_]
        ),
        T = o,
        y = !1;
      return (
        C.followsViewer.state === r(d[12]).FOLLOW_STATUS_NOT_FOLLOWING &&
          ((T = l), (y = !0)),
        a(d[3]).createElement(
          a(d[3]).Fragment,
          null,
          a(d[3]).createElement(
            r(d[4]).Button,
            {
              color: "ig-secondary-button",
              disabled: y,
              loading: !C.followsViewer.stable,
              onClick: p,
            },
            T
          ),
          b &&
            a(d[3]).createElement(t, { onCancel: S, onConfirm: v, userId: f })
        )
      );
    };
  },
  13434895,
  [
    9895940,
    5,
    9895966,
    3,
    9895962,
    9895946,
    10289256,
    9895953,
    10158088,
    10158092,
    69,
    10158304,
    10158089,
  ]
);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var t = function (t) {
      var c = t.className,
        n = t.children;
      return a(d[1]).createElement("h2", { className: i(d[2])("JJF77", c) }, n);
    };
    e.default = t;
  },
  10748049,
  [10748052, 3, 9895958]
);
__d(function () {}, 10748052, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var n = r(d[5]).connect(function (n, t) {
      return {
        onTimingSpinner: function (o) {
          var u = n.navigation,
            c = u.pageIdentifier,
            f = u.route;
          null != f &&
            "" !== f &&
            c &&
            r(d[4]).logComponentPerformanceTiming({
              component: t.component,
              eventType: t.timingEvent,
              pageId: c,
              route: f,
              timeTaken: o,
            });
        },
      };
    })(function (n) {
      n.component;
      var t = n.onTimingSpinner,
        o =
          (n.timingEvent,
          i(d[0])(n, ["component", "onTimingSpinner", "timingEvent"])),
        u = a(d[1]).useRef();
      return (
        a(d[1]).useEffect(
          function () {
            u.current = t;
          },
          [t]
        ),
        a(d[1]).useEffect(function () {
          var n = r(d[2]).now();
          return function () {
            var t = u.current;
            null != t && t(r(d[2]).now() - n);
          };
        }, []),
        a(d[1]).createElement(r(d[3]).Spinner, o)
      );
    });
    e.default = n;
  },
  10289183,
  [9764901, 3, 10289196, 9895962, 10289197, 5]
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
    function o(t) {
      var n,
        o = r(d[14]).matchPath(t, { path: "/:username/hashtag_following/" });
      return null === o || void 0 === o
        ? void 0
        : null === (n = o.params) || void 0 === n
        ? void 0
        : n.username;
    }
    Object.defineProperty(e, "__esModule", { value: !0 }), r(d[0]);
    var l = (function (t) {
        function n() {
          return t.apply(this, arguments) || this;
        }
        i(d[2])(n, t);
        var o = n.prototype;
        return (
          (o.componentDidMount = function () {
            r(d[3]).logPageView(i(d[4]).hashtagFollowList);
          }),
          (o.getEmptyState = function () {
            var t = this.props,
              n = t.userId,
              o = t.username,
              l = n === t.viewerId,
              s = l ? r(d[5])(1049) : r(d[5])(152),
              c = l
                ? r(d[5])(2633)
                : r(d[5])(680, {
                    username: a(d[6]).createElement(
                      r(d[7]).Text,
                      { weight: "semibold" },
                      o
                    ),
                  });
            return a(d[6]).createElement(i(d[8]), {
              icon: a(d[6]).createElement(
                "div",
                { className: "d-Vzv" },
                a(d[6]).createElement("span", { className: "_8324F" }, "#")
              ),
              subtitle: c,
              title: s,
            });
          }),
          (o.render = function () {
            if (this.props.isLoading)
              return a(d[6]).createElement(
                r(d[7]).Box,
                { margin: "auto", marginTop: 12 },
                a(d[6]).createElement(r(d[7]).Spinner, { size: "large" })
              );
            var t =
                this.props.viewerId === this.props.userId
                  ? "self_following_hashtags"
                  : "following_hashtags",
              n = this.props.tagList;
            if (n.length < 1) return this.getEmptyState();
            var o = n.map(function (n) {
              var o = n.id,
                l = n.name,
                s = n.postCount,
                c = n.profilePictureUrl,
                u = a(d[6]).createElement(i(d[9]), {
                  className: "n5B_7",
                  isLink: !0,
                  profilePictureUrl: c,
                  size: 30,
                  tagName: l,
                }),
                p = a(d[6]).createElement(i(d[10]), {
                  id: o,
                  loggingClickPoint: "following_list_follow_button",
                  loggingContainerModule: t,
                  tagName: l,
                });
              return a(d[6]).createElement(r(d[7]).ListItem, {
                action: p,
                icon: u,
                key: l,
                subtitle: a(d[6]).createElement(i(d[11]), {
                  value: s,
                  variant: "unstyled",
                }),
                title: a(d[6]).createElement(
                  r(d[7]).Text.BodyEmphasized,
                  null,
                  a(d[6]).createElement(i(d[12]), {
                    className: "hI7cq",
                    tag: l,
                  })
                ),
              });
            });
            return a(d[6]).createElement(i(d[13]), { className: "_8zyFd" }, o);
          }),
          n
        );
      })(a(d[6]).Component),
      s = r(d[14]).withRouter(
        r(d[18]).connect(function (t, l) {
          var s = l.match,
            c = i(d[15])(o(s.path)),
            u = r(d[16]).getUserByUsername(t, c),
            p = u && u.id,
            f = r(d[16]).getViewer(t),
            h = t.hashtagFollowList.get(p),
            v = [];
          return (
            (
              (null === h || void 0 === h ? void 0 : h.followList) ||
              r(d[17]).EMPTY_LIST
            )
              .toSeq()
              .forEach(function (o) {
                var l = t.tags.get(o);
                null != l && v.push(n({}, l, { name: o }));
              }),
            {
              isLoading: !!(null === h || void 0 === h ? void 0 : h.isLoading),
              tagList: v,
              userId: p,
              username: c,
              viewerId: i(d[15])(f && f.id),
            }
          );
        }, null)(l)
      );
    e.default = s;
  },
  13434886,
  [
    13434896,
    9764888,
    9764914,
    9764900,
    9895951,
    9895940,
    3,
    9895962,
    13434893,
    9895945,
    13434897,
    10158384,
    10092575,
    13434889,
    6,
    9895943,
    9895966,
    13434898,
    5,
  ]
);
__d(function () {}, 13434896, []);
__d(
  function (g, r, i, a, m, e, d) {
    "use strict";
    Object.defineProperty(e, "__esModule", { value: !0 });
    var o = (function (o) {
        function t(t) {
          var n;
          return (
            (n = o.call(this, t) || this),
            (n.$TagFollowButton2 = function (o) {
              var t = n.props,
                l = t.id,
                u = t.isFollowing,
                s = t.isLoading,
                c = t.loggingClickPoint,
                h = t.loggingContainerModule,
                f = t.tagName;
              if (t.viewerLoggedIn) {
                if (!s) {
                  var w = { containerModule: h, clickPoint: c, entityId: l };
                  u
                    ? n.props.onUnfollowHashtag(f, w)
                    : n.props.onFollowHashtag(f, w);
                }
              } else n.props.history.push(n.$TagFollowButton1());
            }),
            (n.state = { initialPath: t.history.location.pathname }),
            n
          );
        }
        i(d[0])(t, o);
        var n = t.prototype;
        return (
          (n.$TagFollowButton1 = function () {
            return r(d[1]).buildLoginLink(this.state.initialPath, {
              source: "followHashtag",
            });
          }),
          (n.render = function () {
            var o = this.props,
              t = o.isFollowing,
              n = o.isLoading,
              l = o.viewerLoggedIn;
            return a(d[2]).createElement(
              r(d[3]).Button,
              {
                color: t ? "ig-secondary-button" : "ig-primary-button",
                disabled: n,
                fullWidth: !0,
                href: l ? void 0 : this.$TagFollowButton1(),
                loading: n,
                onClick: l ? this.$TagFollowButton2 : void 0,
              },
              t && l ? r(d[4]).FOLLOWING_TEXT : r(d[4]).FOLLOW_TEXT
            );
          }),
          t
        );
      })(a(d[2]).Component),
      t = r(d[7]).withRouter(
        r(d[8]).connect(
          function (o, t) {
            var n = r(d[5]).getViewer(o),
              l = !(!n || !n.id),
              u = o.tags.get(t.tagName);
            return {
              id: null === u || void 0 === u ? void 0 : u.id,
              isFollowing: null === u || void 0 === u ? void 0 : u.isFollowing,
              isLoading: null === u || void 0 === u ? void 0 : u.isLoading,
              viewerLoggedIn: l,
            };
          },
          function (o) {
            return {
              onFollowHashtag: function (t, n) {
                return o(r(d[6]).followHashtag(t, n));
              },
              onUnfollowHashtag: function (t, n) {
                return o(r(d[6]).unfollowHashtag(t, n));
              },
            };
          }
        )(o)
      );
    e.default = t;
  },
  13434897,
  [9764914, 9895959, 3, 9895962, 9895953, 9895966, 13434899, 6, 5]
);
