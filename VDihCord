<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DIHCORD</title>
<meta name="dih-lock-seal" content="DIH-V15-LOCK-SEAL-20260414">
<style>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600;700&family=Playfair+Display:wght@700;900&family=DM+Sans:wght@400;500;600;700&display=swap');
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
:root{--bg:#eef2f7;--bg2:#ffffff;--bg3:#f6f8fb;--bg4:#edf1f7;--bg5:#e6ebf2;--border:#cfd8e6;--soft:#d9e2ef;--t1:#16202f;--t2:#334155;--t3:#64748b;--accent:#5865f2;--accent2:#4752c4;--red:#ed4245;--green:#3ba55d;--gold:#c9a84c;--purple:#9b59b6;--orange:#faa81a;--font:'DM Sans',sans-serif;--mono:'IBM Plex Mono',monospace;--display:'DM Sans',sans-serif}
html,body{height:100%;background:var(--bg);color:var(--t1);font-family:var(--font);font-size:14px;overflow:hidden}.hidden{display:none!important}
body.dark-theme{--bg:#313338;--bg2:#2b2d31;--bg3:#232428;--bg4:#383a40;--bg5:#1e1f22;--border:#1b1d22;--soft:#404249;--t1:#f2f3f5;--t2:#dbdee1;--t3:#949ba4}
.auth-screen{position:fixed;inset:0;background:var(--bg);display:flex;align-items:center;justify-content:center;z-index:100;opacity:0;transition:opacity .4s}.auth-screen.visible{opacity:1}
.auth-bg{position:absolute;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 50px,rgba(94,142,214,.02) 50px,rgba(94,142,214,.02) 51px),repeating-linear-gradient(90deg,transparent,transparent 50px,rgba(94,142,214,.02) 50px,rgba(94,142,214,.02) 51px)}
.auth-card{position:relative;z-index:1;width:420px;max-width:92vw;background:var(--bg2);border:1px solid var(--border);border-radius:8px;padding:40px 36px}
.auth-logo{text-align:center;margin-bottom:28px}.auth-logo-icon{font-size:42px;margin-bottom:8px}.auth-logo-title{font-family:var(--display);font-size:28px;font-weight:900;color:var(--accent);letter-spacing:2px}.auth-logo-sub{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:2px;margin-top:4px}
.auth-tabs{display:flex;margin-bottom:24px;border-bottom:1px solid var(--border)}.auth-tab{flex:1;padding:10px;text-align:center;font-family:var(--mono);font-size:12px;font-weight:600;letter-spacing:1px;cursor:pointer;color:var(--t3);border-bottom:2px solid transparent}.auth-tab.active{color:var(--accent);border-bottom-color:var(--accent)}
.auth-field{margin-bottom:14px}.auth-label{display:block;font-family:var(--mono);font-size:10px;font-weight:600;color:var(--t3);letter-spacing:1.5px;text-transform:uppercase;margin-bottom:5px}
.auth-input{width:100%;padding:11px 14px;background:var(--bg);border:1px solid var(--border);color:var(--t1);font-family:var(--mono);font-size:13px;outline:none;border-radius:4px}.auth-input:focus{border-color:var(--accent)}.auth-input::placeholder{color:var(--t3)}
.auth-btn{width:100%;padding:12px;background:var(--accent);color:#fff;border:none;border-radius:4px;cursor:pointer;font-family:var(--mono);font-size:12px;font-weight:700;letter-spacing:2px;text-transform:uppercase;margin-top:8px}.auth-btn:hover{background:var(--accent2)}.auth-btn:disabled{opacity:.5}
.auth-error{font-family:var(--mono);font-size:12px;color:var(--red);text-align:center;margin-top:10px;min-height:18px}.auth-footer{text-align:center;margin-top:20px;font-family:var(--mono);font-size:10px;color:var(--t3)}
.shake{animation:shake .4s}@keyframes shake{0%,100%{transform:translateX(0)}25%{transform:translateX(-8px)}75%{transform:translateX(8px)}}
.app{display:flex;height:100vh;background:var(--bg5)}
.dc-channels{width:240px;min-width:240px;background:var(--bg5);border-right:1px solid #111214;display:flex;flex-direction:column}
.dc-ch-header{padding:16px;font-family:var(--display);font-size:16px;font-weight:800;border-bottom:1px solid #202225;display:flex;align-items:center;gap:8px;letter-spacing:.3px;background:linear-gradient(135deg,rgba(88,101,242,.28),rgba(255,255,255,.03) 55%,transparent)}
.dc-server-card{margin:10px 10px 6px;padding:12px;border:1px solid rgba(255,255,255,.06);border-radius:12px;background:linear-gradient(160deg,rgba(88,101,242,.18),rgba(35,36,40,.95));box-shadow:0 10px 30px rgba(0,0,0,.18)}
.dc-server-name{font-size:15px;font-weight:800}.dc-server-sub{font-size:11px;color:var(--t3);margin-top:4px;line-height:1.4}
.dc-stats-row{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:8px;margin-top:10px}.dc-stat-pill{padding:8px 6px;border-radius:10px;background:rgba(255,255,255,.05);text-align:center}.dc-stat-num{font-size:15px;font-weight:800}.dc-stat-lbl{font-size:10px;color:var(--t3);font-family:var(--mono);letter-spacing:1px;text-transform:uppercase}
.dc-search-shell{padding:0 10px 8px}.dc-filter{width:100%;padding:10px 12px;border-radius:10px;border:1px solid rgba(255,255,255,.06);background:rgba(255,255,255,.04);color:var(--t1);outline:none;font-size:13px}.dc-filter:focus{border-color:rgba(88,101,242,.75)}.dc-filter::placeholder{color:var(--t3)}
.dc-cats{flex:1;overflow-y:auto;padding:4px 0 8px}
.dc-cat-title{padding:8px 16px 4px;font-family:var(--mono);font-size:10px;font-weight:700;color:var(--t3);letter-spacing:1.2px;cursor:pointer;user-select:none;display:flex;align-items:center;gap:4px}.dc-cat-title::before{content:'▾';font-size:8px;transition:transform .2s}.dc-cat-collapsed .dc-cat-title::before{transform:rotate(-90deg)}.dc-cat-collapsed .dc-ch-item{display:none}
.dc-ch-item{display:flex;align-items:center;gap:8px;padding:6px 10px;margin:1px 8px;border-radius:4px;cursor:pointer;font-size:14px;color:var(--t3);transition:all .12s}.dc-ch-item:hover{background:var(--soft);color:var(--t2)}.dc-ch-item.dc-active{background:#404249;color:var(--t1)}
.dc-vote-hot{margin:10px 8px 8px;padding:12px 10px;border-radius:14px;border:1px solid rgba(201,168,76,.28);background:linear-gradient(140deg,rgba(201,168,76,.18),rgba(88,101,242,.12));color:var(--t1);box-shadow:0 12px 28px rgba(0,0,0,.16)}.dc-vote-hot .dc-hash{color:var(--gold);opacity:1}.dc-vote-hot .dc-dm-preview{color:var(--t2)}
.dc-hash{font-size:17px;font-weight:700;opacity:.4;font-family:var(--mono)}.dc-ch-add{padding:6px 24px;font-size:11px;color:var(--accent);cursor:pointer;opacity:.6;font-family:var(--mono)}.dc-ch-add:hover{opacity:1}
.dc-bridge{color:var(--gold)!important}.dc-bridge .dc-hash{color:var(--gold);opacity:.7}.dc-bridge.dc-active{background:rgba(201,168,76,.12)!important}
.dc-dm-av{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;color:#0b0d12;flex-shrink:0}.dc-dm-start{opacity:.4;font-size:13px}.dc-dm-start:hover{opacity:.7}
.dc-nav-item{display:flex;align-items:center;gap:10px;padding:8px 12px;margin:1px 8px;border-radius:4px;cursor:pointer;font-size:13px;font-weight:600;color:var(--t3);transition:all .12s;border-top:1px solid #202225;margin-top:8px;padding-top:12px}.dc-nav-item:hover{background:var(--soft);color:var(--t2)}.dc-nav-item.dc-active{color:var(--t1);background:#404249}
.dc-nav-shell{margin:8px 8px 0;border-top:1px solid #202225;padding-top:8px}.dc-nav-toggle{width:100%;display:flex;align-items:center;justify-content:space-between;gap:8px;padding:8px 10px;border-radius:10px;border:1px solid rgba(255,255,255,.06);background:rgba(255,255,255,.04);color:var(--t2);cursor:pointer;font-family:var(--mono);font-size:11px;letter-spacing:1px;text-transform:uppercase}.dc-nav-toggle:hover{background:rgba(255,255,255,.08);color:var(--t1)}.dc-nav-links{overflow:hidden;transition:max-height .24s ease,opacity .24s ease,transform .24s ease;transform-origin:top}.dc-nav-shell.collapsed .dc-nav-links{max-height:0;opacity:0;transform:translateY(-6px);pointer-events:none}.dc-nav-shell.expanded .dc-nav-links{max-height:420px;opacity:1;transform:translateY(0)}.dc-prefix-badge{display:inline-flex;align-items:center;padding:2px 6px;border-radius:999px;background:rgba(88,101,242,.12);color:var(--accent);font-family:var(--mono);font-size:10px;font-weight:700;letter-spacing:.8px;margin-right:6px}
.dc-user-panel{margin-top:auto;padding:10px 12px;background:#232428;display:flex;align-items:center;gap:10px;border-top:1px solid #1a1b1e}.dc-user-av{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;color:#0b0d12;flex-shrink:0}.dc-user-info{flex:1;overflow:hidden}.dc-user-nm{font-size:13px;font-weight:700;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}.dc-user-id{font-family:var(--mono);font-size:10px;color:var(--t3)}.dc-user-standing{margin-top:6px}.dc-user-actions{display:flex;align-items:center;gap:4px}.dc-theme-btn,.dc-logout{background:none;border:none;color:var(--t3);cursor:pointer;font-size:14px;padding:6px;border-radius:6px}.dc-theme-btn:hover,.dc-logout:hover{color:var(--t1);background:rgba(255,255,255,.06)}
.dc-main{flex:1;display:flex;flex-direction:column;background:radial-gradient(circle at top,rgba(88,101,242,.08),transparent 24%),var(--bg2);position:relative}.dc-main-empty{display:flex;flex-direction:column;align-items:center;justify-content:center;height:100%;color:var(--t3);gap:8px}.dc-empty-icon{font-size:48px;opacity:.3}
.dc-home{padding:28px 30px;overflow-y:auto;flex:1}.dc-home-hero{padding:24px;border:1px solid rgba(255,255,255,.07);border-radius:18px;background:linear-gradient(140deg,rgba(88,101,242,.22),rgba(35,36,40,.96) 55%,rgba(201,168,76,.09));box-shadow:0 16px 40px rgba(0,0,0,.18)}.dc-home-kicker{font-family:var(--mono);font-size:11px;letter-spacing:2px;color:#b8bfff;text-transform:uppercase}.dc-home-title{font-size:30px;font-weight:900;margin-top:8px}.dc-home-text{font-size:14px;color:var(--t2);line-height:1.7;max-width:720px;margin-top:10px}
.dc-home-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px;margin-top:18px}.dc-home-card{padding:16px;border-radius:16px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06)}.dc-home-card h3{font-size:14px;margin-bottom:8px}.dc-home-card p{font-size:13px;color:var(--t2);line-height:1.6}.dc-home-list{margin-top:10px;display:flex;flex-direction:column;gap:8px}.dc-home-link{display:flex;align-items:center;justify-content:space-between;gap:8px;padding:9px 11px;border-radius:10px;background:rgba(255,255,255,.03);cursor:pointer;color:var(--t2)}.dc-home-link:hover{background:rgba(255,255,255,.07);color:var(--t1)}
.dc-header{padding:14px 20px;border-bottom:1px solid #232428;display:flex;align-items:center;gap:10px;background:rgba(0,0,0,.08);box-shadow:0 1px 0 rgba(255,255,255,.02)}.dc-h-icon{font-size:18px;font-weight:700;color:var(--t3);font-family:var(--mono)}.dc-h-name{font-size:16px;font-weight:800}.dc-h-desc{font-size:12px;color:var(--t3);flex:1}.dc-h-tag{font-family:var(--mono);font-size:9px;padding:2px 8px;border-radius:999px;background:var(--gold);color:#0b0d12;font-weight:700}.dc-h-actions{display:flex;gap:4px;margin-left:auto}.dc-h-btn{background:none;border:none;font-size:16px;cursor:pointer;padding:6px 8px;border-radius:4px;color:var(--t3)}.dc-h-btn:hover{background:var(--soft);color:var(--t2)}
.dc-channels{width:280px;min-width:280px}
.dc-nav-shell{margin:10px 8px 0;padding-top:10px;border-top:1px solid rgba(255,255,255,.06)}
.dc-nav-links{display:grid;gap:8px;padding-top:10px}
.dc-nav-item{margin:0;padding:10px 12px;border:1px solid rgba(255,255,255,.06);border-top:none;border-radius:12px;background:rgba(255,255,255,.03)}
.dc-user-panel{padding:12px 14px;border-top:1px solid rgba(255,255,255,.06);background:linear-gradient(180deg,rgba(255,255,255,.04),rgba(255,255,255,.02))}
.dc-user-actions{gap:6px}
.dc-theme-btn,.dc-logout{padding:8px 10px;border:1px solid rgba(255,255,255,.06);background:rgba(255,255,255,.03)}
.dc-h-actions{gap:8px;margin-left:auto;padding:4px;border-radius:14px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06)}
.dc-h-btn{display:flex;align-items:center;gap:6px;padding:8px 10px;border-radius:10px;font-family:var(--mono);font-size:11px;letter-spacing:.6px;text-transform:uppercase}
.dc-h-btn span:last-child{opacity:.9}
.dc-dm-meta{display:flex;align-items:center;gap:10px;min-width:0;flex:1}
.dc-dm-copy{display:flex;flex-direction:column;gap:2px;min-width:0;flex:1}
.dc-dm-name{min-width:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.dc-dm-preview{font-size:11px;color:var(--t3);min-width:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.dc-dm-side{display:flex;flex-direction:column;align-items:flex-end;gap:6px;flex-shrink:0}
.dc-dm-time{font-family:var(--mono);font-size:10px;color:var(--t3)}
.dc-unread-badge{margin-left:auto;min-width:20px;height:20px;padding:0 6px;border-radius:999px;background:var(--accent);color:#fff;display:inline-flex;align-items:center;justify-content:center;font-family:var(--mono);font-size:10px;font-weight:700;letter-spacing:.3px;box-shadow:0 8px 18px rgba(88,101,242,.28)}
.dc-ch-item.dc-unread{color:var(--t1);background:rgba(88,101,242,.08)}
.dc-ch-item.dc-unread .dc-dm-av{box-shadow:0 0 0 2px rgba(88,101,242,.22)}
.dc-ch-item.dc-fav .dc-hash{opacity:.9;color:var(--gold)}
.dc-main{overflow:hidden}
.dc-header{flex-wrap:wrap}
.dc-h-desc{min-width:180px}
.dc-h-btn.active{background:rgba(88,101,242,.12);color:var(--t1)}
.dc-welcome{padding:20px 0 12px}.dc-welcome-icon{font-size:38px;font-weight:900;color:var(--t3)}.dc-welcome-title{font-size:20px;font-weight:700;margin-bottom:4px}.dc-welcome-desc{font-size:13px;color:var(--t3)}
.dc-msgs{flex:1;overflow-y:auto;padding:0 12px 8px;display:flex;flex-direction:column}
.dc-msg-group{display:flex;gap:14px;padding:4px 8px;margin-top:10px;border-radius:4px;position:relative}.dc-msg-group:hover{background:rgba(255,255,255,.03)}
.dc-msg-av{width:40px;height:40px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:15px;font-weight:700;color:#0b0d12;flex-shrink:0;margin-top:2px}.dc-msg-body{flex:1;min-width:0}.dc-msg-row{display:flex;align-items:baseline;gap:6px;flex-wrap:wrap;position:relative}
.dc-msg-author{font-size:14px;font-weight:600;cursor:pointer}.dc-msg-author:hover{text-decoration:underline}.dc-msg-ts{font-family:var(--mono);font-size:11px;color:var(--t3)}.dc-msg-text{font-size:14px;line-height:1.5;color:var(--t2);word-break:break-word;margin-top:1px}
.dc-msg-compact{margin-top:1px;position:relative}.dc-compact-time{position:absolute;left:-50px;top:2px;font-family:var(--mono);font-size:10px;color:transparent}.dc-msg-group:hover .dc-compact-time{color:var(--t3)}.dc-edited{font-size:10px;color:var(--t3);font-family:var(--mono)}
.dc-role-badge{font-family:var(--mono);font-size:9px;padding:1px 6px;border-radius:3px;color:#fff;font-weight:600;margin-left:2px;vertical-align:middle}.dc-plat-badge{font-family:var(--mono);font-size:9px;padding:1px 6px;border-radius:3px;font-weight:700;margin-left:4px;vertical-align:middle}.plat-alyon{background:var(--gold);color:#0b0d12}.plat-chaty{background:var(--accent);color:#fff}
.dc-msg-actions{position:absolute;top:-12px;right:4px;display:none;background:var(--bg3);border:1px solid var(--border);border-radius:4px;padding:2px;z-index:5}.dc-msg-group:hover .dc-msg-actions,.dc-msg-compact:hover .dc-msg-actions{display:flex}
.dc-act-btn{background:none;border:none;font-size:14px;cursor:pointer;padding:4px 6px;border-radius:3px;line-height:1}.dc-act-btn:hover{background:rgba(255,255,255,.1)}.dc-act-btn.active{background:rgba(88,101,242,.14);color:var(--t1)}
.dc-reactions{display:flex;flex-wrap:wrap;gap:4px;margin-top:4px}.dc-react-btn{background:rgba(255,255,255,.05);border:1px solid var(--border);border-radius:6px;padding:2px 8px;font-size:13px;cursor:pointer;color:var(--t2)}.dc-react-btn:hover{background:rgba(255,255,255,.1)}.dc-react-mine{background:rgba(94,142,214,.15);border-color:rgba(94,142,214,.4)}
.dc-react-picker{position:absolute;top:-10px;right:50px;background:var(--bg3);border:1px solid var(--border);border-radius:12px;padding:8px;display:grid;grid-template-columns:repeat(8,32px);gap:4px;z-index:10;max-width:292px;max-height:230px;overflow-y:auto;box-shadow:0 4px 16px rgba(0,0,0,.4)}.dc-react-emoji{width:32px;height:32px;background:none;border:none;font-size:20px;cursor:pointer;padding:4px;border-radius:8px;display:flex;align-items:center;justify-content:center}.dc-react-emoji:hover{background:rgba(255,255,255,.1)}
.dc-reply-bar{display:flex;align-items:center;justify-content:space-between;padding:8px 20px;background:var(--bg3);border-top:1px solid var(--border);font-size:13px;color:var(--t2)}.dc-reply-cancel{background:none;border:none;color:var(--t3);cursor:pointer;font-size:16px}.dc-reply-cancel:hover{color:var(--t1)}
.dc-typing{min-height:20px;padding:0 20px;font-size:12px;color:var(--t3)}.dc-typing-dots{animation:blink 1.4s infinite;font-size:10px;letter-spacing:2px}@keyframes blink{0%,100%{opacity:.2}50%{opacity:1}}
.dc-input-area{padding:0 16px 20px}.dc-input-shell{background:var(--bg4);border:1px solid #45474f;border-radius:8px;overflow:hidden}.dc-input-wrap{display:flex;align-items:center;padding:2px 6px}.dc-input-btn{width:38px;height:38px;border:none;border-radius:10px;background:rgba(255,255,255,.05);color:var(--t2);cursor:pointer;display:inline-flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}.dc-input-btn:hover{background:rgba(255,255,255,.1);color:var(--t1)}.dc-input-btn:disabled{opacity:.45;cursor:not-allowed}.dc-input{flex:1;padding:13px 14px;background:transparent;border:none;color:var(--t1);font-family:var(--font);font-size:15px;outline:none}.dc-input::placeholder{color:var(--t3)}.dc-input:disabled{opacity:.4}.dc-upload-preview{display:flex;align-items:center;gap:12px;padding:0 14px 12px}.dc-upload-thumb{width:56px;height:56px;border-radius:12px;object-fit:cover;flex-shrink:0;border:1px solid rgba(255,255,255,.08)}.dc-upload-copy{min-width:0;display:flex;flex-direction:column;gap:4px}.dc-upload-name{font-size:12px;font-weight:700;color:var(--t1);white-space:nowrap;overflow:hidden;text-overflow:ellipsis}.dc-upload-sub{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:.4px;text-transform:uppercase}.dc-upload-clear{margin-left:auto;background:none;border:none;color:var(--t3);cursor:pointer;font-size:16px;padding:6px;border-radius:8px}.dc-upload-clear:hover{background:rgba(255,255,255,.08);color:var(--t1)}.dc-input-meta{display:flex;align-items:center;justify-content:space-between;padding:0 14px 12px 14px;font-size:11px;color:var(--t3);font-family:var(--mono)}.dc-input-limit{color:var(--t3)}.dc-input-limit.dc-limit-warn{color:var(--orange)}.dc-input-limit.dc-limit-bad{color:var(--red)}.dc-input-note{min-height:14px}.dc-input-note.dc-note-error{color:var(--red)}.dc-input-note.dc-note-warn{color:var(--orange)}
.dc-muted-bar{padding:12px 20px;background:rgba(231,76,60,.1);border-top:1px solid rgba(231,76,60,.3);font-size:13px;color:var(--red);text-align:center;font-family:var(--mono)}
.dc-date-div{display:flex;align-items:center;margin:16px 8px 4px;gap:8px}.dc-date-div::before,.dc-date-div::after{content:'';flex:1;height:1px;background:var(--border)}.dc-date-div span{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:1px;white-space:nowrap}
.dc-gif{max-width:350px;max-height:300px;border-radius:8px;margin-top:6px;display:block;cursor:pointer;transition:opacity .15s}.dc-gif:hover{opacity:.85}.dc-link{color:var(--accent);text-decoration:none;word-break:break-all}.dc-link:hover{text-decoration:underline}
.dc-members{width:240px;min-width:240px;background:var(--bg5);border-left:1px solid #111214;overflow-y:auto;padding:12px}.dc-members-title{font-family:var(--mono);font-size:10px;font-weight:700;color:var(--t3);letter-spacing:1.2px;padding:8px 4px 4px}.dc-members-search{margin-bottom:8px}
.dc-member{display:flex;align-items:center;gap:10px;padding:6px 8px;border-radius:4px;margin-bottom:2px;cursor:pointer}.dc-member:hover{background:rgba(255,255,255,.04)}.dc-member-av{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#0b0d12;flex-shrink:0}.dc-member-info{overflow:hidden}.dc-member-name{font-size:13px;font-weight:500}.dc-member-role{font-size:10px;color:var(--t3)}
.dc-pins-panel{position:absolute;top:48px;right:12px;width:340px;max-height:400px;overflow-y:auto;background:var(--bg3);border:1px solid var(--border);border-radius:8px;z-index:20;box-shadow:0 8px 24px rgba(0,0,0,.5)}.dc-pins-header{display:flex;align-items:center;padding:12px 14px;font-weight:700;font-size:14px;border-bottom:1px solid var(--border)}.dc-pin-item{padding:10px 14px;border-bottom:1px solid var(--border);font-size:13px;color:var(--t2)}.dc-pin-item:last-child{border:none}
.dc-toast-stack{position:fixed;right:18px;bottom:18px;display:flex;flex-direction:column;gap:10px;z-index:90;pointer-events:none}
.dc-toast{width:min(320px,calc(100vw - 32px));padding:12px 14px;border-radius:16px;border:1px solid rgba(255,255,255,.08);background:linear-gradient(180deg,rgba(35,36,40,.96),rgba(24,25,28,.96));box-shadow:0 18px 40px rgba(0,0,0,.35);pointer-events:auto;cursor:pointer}
.dc-toast-title{font-size:13px;font-weight:800;color:var(--t1)}
.dc-toast-body{margin-top:4px;font-size:12px;color:var(--t2);line-height:1.5}
.dc-toast-meta{margin-top:8px;font-family:var(--mono);font-size:10px;letter-spacing:.8px;text-transform:uppercase;color:var(--t3)}
.forum-shell{padding:22px 24px;overflow-y:auto;flex:1;display:flex;flex-direction:column;gap:18px}
.forum-hero{padding:20px 22px;border-radius:18px;border:1px solid rgba(255,255,255,.07);background:linear-gradient(145deg,rgba(88,101,242,.18),rgba(35,36,40,.95) 60%,rgba(255,255,255,.03))}
.forum-title{font-size:26px;font-weight:900}
.forum-sub{margin-top:8px;font-size:14px;color:var(--t2);line-height:1.7;max-width:760px}
.forum-grid{display:grid;grid-template-columns:minmax(0,1.1fr) minmax(320px,.9fr);gap:18px;align-items:start}
.forum-col{display:flex;flex-direction:column;gap:16px;min-width:0}
.forum-card{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06);border-radius:18px;padding:16px;min-width:0}
.forum-card-head{display:flex;align-items:flex-start;justify-content:space-between;gap:10px;margin-bottom:12px}
.forum-card-title{font-size:15px;font-weight:800}
.forum-card-sub{font-size:11px;color:var(--t3);font-family:var(--mono)}
.forum-list{display:flex;flex-direction:column;gap:10px}
.forum-topic{padding:14px 14px 12px;border-radius:14px;border:1px solid rgba(255,255,255,.06);background:rgba(255,255,255,.03);cursor:pointer}
.forum-topic:hover{background:rgba(255,255,255,.06)}
.forum-topic.active{border-color:rgba(88,101,242,.45);background:rgba(88,101,242,.1)}
.forum-topic-top{display:flex;align-items:flex-start;justify-content:space-between;gap:10px}
.forum-topic-title{font-size:15px;font-weight:800;line-height:1.4}
.forum-topic-meta{margin-top:8px;font-size:11px;color:var(--t3);font-family:var(--mono)}
.forum-topic-body{margin-top:8px;font-size:13px;color:var(--t2);line-height:1.6}
.forum-pill{display:inline-flex;align-items:center;justify-content:center;min-width:28px;height:22px;padding:0 8px;border-radius:999px;background:rgba(88,101,242,.12);color:var(--accent);font-family:var(--mono);font-size:10px;font-weight:700}
.forum-empty{padding:18px;border-radius:14px;background:rgba(255,255,255,.03);border:1px dashed rgba(255,255,255,.08);font-size:13px;color:var(--t3);text-align:center}
.forum-form{display:flex;flex-direction:column;gap:10px}
.forum-thread{display:flex;flex-direction:column;gap:12px}
.forum-post{padding:14px;border-radius:14px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06)}
.forum-post-head{display:flex;align-items:flex-start;justify-content:space-between;gap:10px}
.forum-post-author{font-weight:800}
.forum-post-time{font-family:var(--mono);font-size:10px;color:var(--t3)}
.forum-post-body{margin-top:8px;font-size:13px;color:var(--t2);line-height:1.7;white-space:pre-wrap;word-break:break-word}
.forum-thread-actions{display:flex;gap:8px;flex-wrap:wrap}
.forum-replies{display:flex;flex-direction:column;gap:10px}
.forum-reply{padding:12px 14px;border-radius:12px;background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.05)}
.forum-reply-box{display:flex;flex-direction:column;gap:10px}
.forum-quick{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:8px}
.forum-quick .dc-home-link{padding:10px 12px}
.forum-badges{display:flex;align-items:center;gap:8px;flex-wrap:wrap;margin-top:8px}
.forum-badge{display:inline-flex;align-items:center;padding:3px 8px;border-radius:999px;background:rgba(88,101,242,.12);color:var(--accent);font-family:var(--mono);font-size:10px;font-weight:700;letter-spacing:.5px;text-transform:uppercase}
.forum-badge.forum-locked{background:rgba(250,168,26,.15);color:var(--orange)}
.forum-badge.forum-pinned{background:rgba(201,168,76,.15);color:var(--gold)}
.site-shell{padding:24px 28px;overflow-y:auto;flex:1}
.site-hero{padding:22px 24px;border-radius:18px;border:1px solid rgba(255,255,255,.07);background:linear-gradient(145deg,rgba(88,101,242,.18),rgba(35,36,40,.95) 60%,rgba(255,255,255,.03))}
.site-title{font-size:26px;font-weight:900}
.site-sub{margin-top:8px;font-size:14px;color:var(--t2);line-height:1.7;max-width:760px}
.site-grid{display:grid;gap:16px;max-width:980px;margin-top:18px}
.site-card{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06);border-radius:18px;padding:16px}
.site-card-head{display:flex;align-items:flex-start;justify-content:space-between;gap:10px;margin-bottom:12px;flex-wrap:wrap}
.site-card-title{font-size:15px;font-weight:800}
.site-card-sub{font-size:11px;color:var(--t3);font-family:var(--mono)}
.site-list{display:flex;flex-direction:column;gap:10px}
.site-row{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:12px 0;border-top:1px solid rgba(255,255,255,.06)}
.site-row:first-child{border-top:none;padding-top:0}
.site-row-copy{display:flex;flex-direction:column;gap:4px}
.site-row-title{font-size:13px;font-weight:700}
.site-row-sub{font-size:12px;color:var(--t3);line-height:1.5}
.site-actions{display:flex;align-items:center;gap:8px;flex-wrap:wrap}
.site-select{min-width:160px}
.inbox-item{padding:14px;border-radius:14px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);cursor:pointer}
.inbox-item:hover{background:rgba(255,255,255,.06)}
.inbox-item.unread{border-color:rgba(88,101,242,.4);background:rgba(88,101,242,.08)}
.inbox-top{display:flex;align-items:flex-start;justify-content:space-between;gap:10px}
.inbox-title{font-size:14px;font-weight:800}
.inbox-meta{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:.5px;text-transform:uppercase}
.inbox-body{margin-top:8px;font-size:13px;color:var(--t2);line-height:1.6}
.nav-badge{display:inline-flex;align-items:center;justify-content:center;min-width:18px;height:18px;padding:0 6px;border-radius:999px;background:var(--accent);color:#fff;font-family:var(--mono);font-size:10px;font-weight:700}
.search-panel{position:absolute;top:62px;right:14px;width:min(440px,calc(100vw - 28px));max-height:70vh;overflow-y:auto;background:var(--bg3);border:1px solid var(--border);border-radius:16px;z-index:40;box-shadow:0 16px 40px rgba(0,0,0,.35)}
.search-head{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:14px;border-bottom:1px solid var(--border)}
.search-body{padding:14px;display:flex;flex-direction:column;gap:12px}
.search-form{display:grid;grid-template-columns:minmax(0,1fr) 120px;gap:10px}
.search-result{padding:12px 14px;border-radius:12px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);cursor:pointer}
.search-result:hover{background:rgba(255,255,255,.06)}
.search-result-title{font-size:13px;font-weight:800}
.search-result-meta{margin-top:5px;font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:.5px;text-transform:uppercase}
.search-result-body{margin-top:8px;font-size:12px;color:var(--t2);line-height:1.5}
.poll-shell{margin-top:4px;padding:12px;border-radius:14px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);display:flex;flex-direction:column;gap:10px;min-width:0}
.poll-title{font-size:14px;font-weight:800;line-height:1.5}
.poll-options{display:flex;flex-direction:column;gap:8px}
.poll-option{width:100%;text-align:left;padding:10px 12px;border-radius:12px;border:1px solid rgba(255,255,255,.08);background:rgba(255,255,255,.03);color:var(--t2);cursor:pointer}
.poll-option:hover{background:rgba(255,255,255,.07);color:var(--t1)}
.poll-option:disabled{cursor:not-allowed;opacity:.72}
.poll-option.poll-voted{border-color:rgba(88,101,242,.45);background:rgba(88,101,242,.12);color:var(--t1)}
.poll-option-top{display:flex;align-items:center;justify-content:space-between;gap:10px}
.poll-bar{height:6px;border-radius:999px;background:rgba(255,255,255,.06);overflow:hidden;margin-top:8px}
.poll-bar-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,var(--accent),#7b86ff)}
.poll-meta{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:.5px;text-transform:uppercase}
/* Profile card */
.pf-card{background:var(--bg3);border:1px solid var(--border);border-radius:8px;overflow:hidden;max-width:520px;margin-bottom:20px}.pf-banner{height:80px}.pf-card-body{padding:0 20px 20px;position:relative}.pf-avatar{width:72px;height:72px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:26px;font-weight:700;color:#0b0d12;border:4px solid var(--bg3);margin-top:-36px;margin-bottom:8px}.pf-display-name{font-size:20px;font-weight:700}.pf-username{font-family:var(--mono);font-size:11px;color:var(--t3);margin-top:2px}.pf-divider{height:1px;background:var(--border);margin:10px 0}.pf-section{margin-bottom:10px}.pf-section-title{font-family:var(--mono);font-size:10px;font-weight:700;color:var(--t1);letter-spacing:1px;text-transform:uppercase;margin-bottom:4px}.pf-bio{font-size:13px;color:var(--t2);line-height:1.5;white-space:pre-wrap}.pf-field{font-size:13px;color:var(--t2)}.pf-warning-box{margin-top:6px;padding:12px;border-radius:12px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06)}.pf-warning-row{display:flex;align-items:center;justify-content:space-between;gap:10px;font-size:13px;color:var(--t2);padding:5px 0}.pf-warning-note{margin-top:8px;font-size:12px;color:var(--t3);line-height:1.5}.pf-warning-list{margin-top:10px;display:flex;flex-direction:column;gap:8px}.pf-warning-item{padding:8px 10px;border-radius:10px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.06);font-size:12px;color:var(--t2)}.pf-edit-btn{width:100%;margin-top:12px}
.pf-edit-card{background:var(--bg3);border:1px solid var(--border);border-radius:8px;padding:24px;margin-top:16px;max-width:600px}.pf-edit-banner{height:60px;border-radius:6px}.pf-color-row{display:flex;align-items:center;gap:10px}.pf-color-input{width:40px;height:34px;border:none;background:transparent;cursor:pointer;padding:0}.pf-color-input::-webkit-color-swatch-wrapper{padding:0}.pf-color-input::-webkit-color-swatch{border:2px solid var(--border);border-radius:4px}.pf-color-presets{display:flex;gap:4px}.pf-color-swatch{width:24px;height:24px;border-radius:4px;cursor:pointer;border:2px solid transparent}.pf-color-swatch:hover{border-color:var(--t1)}
/* Admin */
.admin-panel{flex:1;overflow-y:auto;padding:24px 28px}.admin-section{margin-bottom:28px}.admin-title{font-family:var(--mono);font-size:11px;font-weight:700;color:#a5b0ff;letter-spacing:3px;text-transform:uppercase;margin-bottom:14px;padding-bottom:8px;border-bottom:1px solid #3b3d45}
.admin-shell{display:flex;flex-direction:column;gap:18px;max-width:1380px;margin:0 auto;width:100%;min-width:0}.admin-topbar{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;flex-wrap:wrap}.admin-overview{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px}.admin-stat{background:linear-gradient(180deg,rgba(88,101,242,.18),rgba(88,101,242,.05));border:1px solid rgba(255,255,255,.06);border-radius:12px;padding:14px 16px;min-width:0}.admin-stat-label{font-family:var(--mono);font-size:10px;letter-spacing:1.5px;color:var(--t3);text-transform:uppercase}.admin-stat-value{font-size:24px;font-weight:800;margin-top:6px}.admin-grid{display:grid;grid-template-columns:minmax(0,1.15fr) minmax(340px,.85fr);gap:18px;align-items:start}.admin-stack{display:flex;flex-direction:column;gap:18px;min-width:0}.admin-card{background:var(--bg3);border:1px solid rgba(255,255,255,.06);border-radius:14px;padding:16px;box-shadow:0 10px 30px rgba(0,0,0,.12);min-width:0;overflow:hidden}.admin-card-head{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;margin-bottom:12px;flex-wrap:wrap}.admin-card-title{font-size:15px;font-weight:800}.admin-card-sub{font-size:11px;color:var(--t3);font-family:var(--mono)}.admin-list{display:flex;flex-direction:column;gap:10px;min-width:0}.admin-user{display:flex;flex-direction:column;gap:12px;align-items:stretch;padding:12px;border-radius:10px;background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.04);min-width:0}.admin-user-main{min-width:0}.admin-user-line{display:flex;align-items:center;gap:8px;flex-wrap:wrap}.admin-user-name{font-weight:700;word-break:break-word}.admin-user-meta{font-size:12px;color:var(--t3);margin-top:4px}.admin-mini-list{display:flex;flex-direction:column;gap:8px;min-width:0}.admin-mini-item{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:10px 12px;border-radius:10px;background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.04);flex-wrap:wrap}.admin-log-item{padding:10px 12px;border-radius:10px;background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.04);min-width:0}.admin-log-top{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;margin-bottom:4px;flex-wrap:wrap}.admin-log-title{font-weight:700}.admin-log-meta{font-size:12px;color:var(--t3);word-break:break-word}
.admin-table{width:100%;border-collapse:collapse;font-size:13px}.admin-table th{font-family:var(--mono);font-size:10px;font-weight:600;color:var(--t3);letter-spacing:1.5px;text-transform:uppercase;text-align:left;padding:8px 12px;border-bottom:1px solid var(--border);background:var(--bg3)}.admin-table td{padding:8px 12px;border-bottom:1px solid var(--border);color:var(--t2)}.admin-table tr:hover td{background:var(--bg3)}
.role-tag{font-family:var(--mono);font-size:10px;padding:2px 8px;letter-spacing:1px;text-transform:uppercase;border:1px solid;border-radius:2px}.role-owner{color:var(--gold);border-color:var(--gold)}.role-mod{color:var(--green);border-color:var(--green)}.role-user{color:var(--t3);border-color:var(--t3)}
.status-tag{font-family:var(--mono);font-size:10px;padding:2px 8px;border-radius:2px}.st-banned{color:var(--red);border:1px solid var(--red);background:rgba(231,76,60,.1)}.st-muted{color:var(--orange);border:1px solid var(--orange);background:rgba(230,126,34,.1)}.st-ok{color:var(--green)}.warn-chip{display:inline-flex;align-items:center;gap:6px;padding:4px 8px;border-radius:999px;font-family:var(--mono);font-size:10px;font-weight:700;letter-spacing:1px;text-transform:uppercase;border:1px solid}.warn-good{color:var(--green);border-color:rgba(59,165,93,.55);background:rgba(59,165,93,.12)}.warn-warn{color:var(--orange);border-color:rgba(250,168,26,.55);background:rgba(250,168,26,.12)}.warn-bad{color:var(--red);border-color:rgba(237,66,69,.55);background:rgba(237,66,69,.12)}
.mono{font-family:var(--mono);font-size:12px;word-break:break-word}.actions-cell{display:flex;gap:6px;align-items:center;flex-wrap:wrap;min-width:0}
.btn-sm{padding:4px 10px;font-family:var(--mono);font-size:10px;font-weight:600;letter-spacing:1px;text-transform:uppercase;border:1px solid;cursor:pointer;background:transparent;transition:all .2s;border-radius:2px}.btn-del{color:var(--red);border-color:var(--red)}.btn-del:hover{background:var(--red);color:#fff}.btn-edit{color:var(--accent);border-color:var(--accent)}.btn-edit:hover{background:var(--accent);color:#fff}.btn-mod{color:var(--green);border-color:var(--green)}.btn-mod:hover{background:var(--green);color:#fff}.btn-warn{color:var(--orange);border-color:var(--orange)}.btn-warn:hover{background:var(--orange);color:#fff}.btn-mute{color:var(--purple);border-color:var(--purple)}.btn-mute:hover{background:var(--purple);color:#fff}.btn-ban{color:var(--red);border-color:var(--red)}.btn-ban:hover{background:var(--red);color:#fff}
.form-block{margin:16px 0;background:var(--bg3);border:1px solid var(--border);padding:20px;border-radius:8px;min-width:0}.form-title{font-size:15px;font-weight:700;margin-bottom:14px}.form-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:12px;min-width:0}.form-label{display:block;font-family:var(--mono);font-size:10px;font-weight:600;color:var(--t3);letter-spacing:1px;text-transform:uppercase;margin-bottom:4px}.form-input{width:100%;padding:10px 12px;background:var(--bg);border:1px solid var(--border);color:var(--t1);font-family:var(--font);font-size:13px;outline:none;border-radius:4px;min-width:0}.form-input:focus{border-color:var(--accent)}.form-textarea{min-height:60px;resize:vertical}
.btn{display:inline-block;padding:10px 20px;border:none;cursor:pointer;font-family:var(--mono);font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;border-radius:4px;transition:all .2s}.btn-accent{background:var(--accent);color:#fff}.btn-accent:hover{background:var(--accent2)}.btn-red{background:var(--red);color:#fff}.btn-outline{background:transparent;border:1px solid var(--border);color:var(--t2)}.btn-outline:hover{border-color:var(--t1);color:var(--t1)}
.admin-msg{font-family:var(--mono);font-size:12px;margin-top:10px;padding:8px 12px;border-radius:4px}.admin-msg.success{color:var(--green);background:rgba(46,204,113,.1)}.admin-msg.error{color:var(--red);background:rgba(231,76,60,.1)}
.site-lock-screen{position:fixed;inset:0;z-index:9998;display:flex;align-items:center;justify-content:center;padding:24px;background:radial-gradient(circle at top,rgba(250,168,26,.16),transparent 28%),linear-gradient(180deg,#0f1116,#090a0d 60%,#040507);backdrop-filter:blur(8px)}.site-lock-card{width:min(640px,100%);padding:30px;border-radius:24px;border:1px solid rgba(250,168,26,.24);background:linear-gradient(180deg,rgba(255,255,255,.05),rgba(255,255,255,.02));box-shadow:0 28px 90px rgba(0,0,0,.45)}.site-lock-kicker{font-family:var(--mono);font-size:11px;letter-spacing:2px;text-transform:uppercase;color:#ffd38a}.site-lock-title{margin-top:10px;font-size:34px;font-weight:900;color:#fff}.site-lock-text{margin-top:12px;font-size:14px;line-height:1.7;color:#d7d9de}.site-lock-reason{margin-top:18px;padding:14px 16px;border-radius:16px;background:rgba(0,0,0,.28);border:1px solid rgba(255,255,255,.06)}.site-lock-label{font-family:var(--mono);font-size:11px;letter-spacing:1px;text-transform:uppercase;color:#ffd38a}.site-lock-note{margin-top:8px;font-size:15px;font-weight:700;color:#fff}.site-lock-meta{margin-top:14px;font-family:var(--mono);font-size:11px;letter-spacing:1px;text-transform:uppercase;color:#9ea5af}.site-lock-admin-note{padding:10px 12px;border-radius:12px;background:rgba(250,168,26,.09);border:1px solid rgba(250,168,26,.2);font-size:12px;color:var(--t2);line-height:1.6}
/* Profile popup */
.pp-overlay{position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:49}.profile-popup{position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background:var(--bg2);border:1px solid var(--border);border-radius:12px;width:360px;max-width:90vw;z-index:50;overflow:hidden;box-shadow:0 12px 40px rgba(0,0,0,.6)}.pp-banner{height:70px}.pp-body{padding:0 20px 20px;position:relative}.pp-avatar{width:64px;height:64px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:22px;font-weight:700;color:#0b0d12;border:4px solid var(--bg2);margin-top:-32px;margin-bottom:8px}.pp-name{font-size:18px;font-weight:700}.pp-id{font-family:var(--mono);font-size:11px;color:var(--t3);margin-top:2px}.pp-bio{font-size:12px;color:var(--t2);margin-top:8px;line-height:1.4;white-space:pre-wrap}.pp-section{margin-top:10px}.pp-mini{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:6px;font-size:12px;color:var(--t2)}.pp-actions{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:8px;margin-top:10px}.pp-close{position:absolute;top:8px;right:12px;background:none;border:none;color:var(--t3);font-size:18px;cursor:pointer}.pp-close:hover{color:var(--t1)}
.av-shell{position:relative;display:inline-flex;align-items:center;justify-content:center;flex-shrink:0}.av-core{position:relative;z-index:2}.av-photo{color:transparent!important;text-shadow:none!important;background-size:cover!important;background-position:center!important}.av-shell::before,.av-shell::after{pointer-events:none;position:absolute;z-index:3;display:none}.av-shell.av-sparkles::before,.av-shell.av-sparkles::after{display:block;content:'✦';color:#ffe38a;text-shadow:0 2px 8px rgba(0,0,0,.25)}.av-shell.av-sparkles::before{top:-5px;left:-4px;font-size:11px}.av-shell.av-sparkles::after{right:-4px;bottom:-5px;font-size:10px}.av-shell.av-crown::before{display:block;content:'♛';top:-13px;left:50%;transform:translateX(-50%);font-size:14px;color:#f6d365;text-shadow:0 2px 10px rgba(0,0,0,.28)}.av-shell.av-orbit::before{display:block;content:'';inset:-4px;border-radius:999px;border:1.5px dashed rgba(88,101,242,.55);box-shadow:0 0 0 1px rgba(255,255,255,.08)}.av-shell.av-ribbon::before{display:block;content:'✿';left:-6px;bottom:-8px;font-size:12px;color:#ff9ecf;text-shadow:0 2px 8px rgba(0,0,0,.28)}.av-shell.av-ribbon::after{display:block;content:'✿';right:-6px;top:-7px;font-size:10px;color:#ffb7dd;text-shadow:0 2px 8px rgba(0,0,0,.28)}.av-shell.av-laurel::before,.av-shell.av-laurel::after{display:block;content:'❖';color:#9fe7c6;text-shadow:0 2px 8px rgba(0,0,0,.22)}.av-shell.av-laurel::before{left:-8px;top:50%;transform:translateY(-50%);font-size:11px}.av-shell.av-laurel::after{right:-8px;top:50%;transform:translateY(-50%);font-size:11px}.av-shell.av-pixel .av-core{box-shadow:0 0 0 2px rgba(255,255,255,.12),0 0 0 4px rgba(88,101,242,.22)}.av-shell.av-confetti::before,.av-shell.av-confetti::after{display:block;color:#ffd166;text-shadow:0 2px 8px rgba(0,0,0,.25)}.av-shell.av-confetti::before{content:'✺';top:-7px;right:-5px;font-size:11px}.av-shell.av-confetti::after{content:'✷';left:-6px;bottom:-7px;font-size:10px;color:#7b86ff}.av-frame-neon .av-core{box-shadow:0 0 0 2px rgba(123,134,255,.72),0 0 18px rgba(123,134,255,.65)}.av-frame-gold .av-core{box-shadow:0 0 0 2px rgba(246,211,101,.9),0 0 18px rgba(201,168,76,.45)}.av-frame-ruby .av-core{box-shadow:0 0 0 2px rgba(237,66,69,.72),0 0 18px rgba(237,66,69,.5)}.av-frame-emerald .av-core{box-shadow:0 0 0 2px rgba(59,165,93,.75),0 0 18px rgba(59,165,93,.5)}.av-frame-frost .av-core{box-shadow:0 0 0 2px rgba(194,231,255,.75),0 0 18px rgba(194,231,255,.45)}.av-frame-glitch .av-core{box-shadow:3px 0 0 rgba(237,66,69,.7),-3px 0 0 rgba(88,101,242,.75),0 0 14px rgba(255,255,255,.22)}.pf-theme-neon{box-shadow:0 0 0 1px rgba(123,134,255,.22),0 24px 70px rgba(88,101,242,.18)}.pf-theme-neon .pf-banner,.pf-theme-neon .pp-banner{background:linear-gradient(120deg,#101225,#5865f2,#1dd1a1)!important}.pf-theme-gold{box-shadow:0 0 0 1px rgba(201,168,76,.28),0 24px 70px rgba(201,168,76,.12)}.pf-theme-gold .pf-banner,.pf-theme-gold .pp-banner{background:linear-gradient(120deg,#1f1a0a,#c9a84c,#3a2d0d)!important}.pf-theme-candy .pf-banner,.pf-theme-candy .pp-banner{background:linear-gradient(120deg,#ff9ecf,#7b86ff,#ffd166)!important}.pf-theme-forest .pf-banner,.pf-theme-forest .pp-banner{background:linear-gradient(120deg,#071d14,#3ba55d,#9fe7c6)!important}.pf-theme-midnight .pf-banner,.pf-theme-midnight .pp-banner{background:linear-gradient(120deg,#080b12,#16202f,#5865f2)!important}.pf-avatar-preview{display:flex;align-items:center;gap:12px;padding:12px 14px;border-radius:14px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.06);margin-top:12px}.pf-avatar-preview-copy{display:flex;flex-direction:column;gap:4px;min-width:0}.pf-avatar-preview-title{font-size:12px;font-weight:700}.pf-avatar-preview-sub{font-family:var(--mono);font-size:10px;color:var(--t3);letter-spacing:.6px;text-transform:uppercase}
.av-shell.av-halo::before{display:block;content:'';top:-8px;left:50%;width:70%;height:8px;transform:translateX(-50%);border:2px solid #f6d365;border-radius:999px;box-shadow:0 0 10px rgba(246,211,101,.65)}.av-shell.av-bolts::before,.av-shell.av-bolts::after{display:block;color:#7b86ff;text-shadow:0 2px 8px rgba(0,0,0,.28)}.av-shell.av-bolts::before{content:'⚡';left:-8px;top:-6px;font-size:12px}.av-shell.av-bolts::after{content:'⚡';right:-8px;bottom:-7px;font-size:11px;color:#ffd166}.av-shell.av-moon::before{display:block;content:'☾';right:-7px;top:-9px;font-size:14px;color:#c2e7ff;text-shadow:0 2px 10px rgba(194,231,255,.45)}
body.fatal-lock{overflow:hidden!important}.fatal-lock-screen{position:fixed;inset:0;z-index:9999;display:flex;align-items:center;justify-content:center;padding:24px;background:radial-gradient(circle at top,rgba(237,66,69,.18),transparent 30%),linear-gradient(180deg,#110d10,#070709 55%,#000)}.fatal-lock-card{width:min(560px,100%);padding:28px;border-radius:20px;border:1px solid rgba(237,66,69,.35);background:linear-gradient(180deg,rgba(255,255,255,.04),rgba(255,255,255,.02));box-shadow:0 24px 80px rgba(0,0,0,.45)}.fatal-lock-kicker{font-family:var(--mono);font-size:11px;letter-spacing:2px;text-transform:uppercase;color:#ff9fa1}.fatal-lock-title{font-size:34px;font-weight:900;letter-spacing:1px;margin-top:10px;color:#fff}.fatal-lock-text{margin-top:12px;font-size:14px;line-height:1.7;color:#d7d9de}.fatal-lock-code{margin-top:16px;padding:12px 14px;border-radius:12px;background:rgba(0,0,0,.35);border:1px solid rgba(255,255,255,.06);font-family:var(--mono);font-size:12px;color:#ffb5b7;word-break:break-word}.fatal-lock-note{margin-top:14px;font-family:var(--mono);font-size:11px;letter-spacing:1px;text-transform:uppercase;color:#8f949e}
body.light-theme .auth-card,body.light-theme .dc-channels,body.light-theme .dc-members,body.light-theme .dc-user-panel,body.light-theme .dc-header,body.light-theme .dc-input-shell,body.light-theme .pf-card,body.light-theme .pf-edit-card,body.light-theme .profile-popup,body.light-theme .admin-card,body.light-theme .admin-stat,body.light-theme .form-block,body.light-theme .dc-pins-panel{box-shadow:none}
body.light-theme .dc-channels,body.light-theme .dc-members{background:var(--bg2);border-color:var(--border)}
body.light-theme .dc-user-panel,body.light-theme .dc-header,body.light-theme .dc-pins-panel,body.light-theme .admin-card,body.light-theme .pf-card,body.light-theme .pf-edit-card,body.light-theme .profile-popup,body.light-theme .form-block{background:var(--bg2);border-color:var(--border)}
body.light-theme .dc-input-shell,body.light-theme .admin-stat{background:var(--bg3);border-color:var(--border)}
body.light-theme .dc-nav-item.dc-active,body.light-theme .dc-ch-item.dc-active{background:rgba(88,101,242,.12);color:var(--accent)}
body.light-theme .dc-msg-group:hover,body.light-theme .dc-member:hover,body.light-theme .dc-home-link,body.light-theme .admin-mini-item,body.light-theme .admin-user,body.light-theme .admin-log-item,body.light-theme .pf-warning-box,body.light-theme .pf-warning-item{background:rgba(15,23,42,.03);border-color:rgba(15,23,42,.08)}
body.light-theme .dc-nav-toggle{background:rgba(15,23,42,.03);border-color:rgba(15,23,42,.08)}
body.light-theme .dc-toast{background:linear-gradient(180deg,rgba(255,255,255,.96),rgba(246,248,251,.98));border-color:rgba(15,23,42,.08);box-shadow:0 18px 40px rgba(15,23,42,.12)}
@media(max-width:1180px){.admin-grid{grid-template-columns:1fr}.admin-card{padding:14px}}
@media(max-width:980px){.admin-topbar{flex-direction:column;align-items:flex-start}.admin-overview{grid-template-columns:repeat(auto-fit,minmax(150px,1fr))}}
@media(max-width:768px){.dc-channels{width:70px;min-width:70px}.dc-ch-header span,.dc-server-card,.dc-search-shell,.dc-cat-title,.dc-ch-add,.dc-user-info,.dc-ch-item span:not(.dc-hash),.dc-nav-item span,.dc-nav-toggle span:last-child{display:none}.dc-ch-item,.dc-nav-item{justify-content:center;padding:8px}.dc-members{display:none}.dc-header{padding:12px 14px}.dc-input-area{padding:0 10px 12px}.dc-home{padding:16px}.dc-home-title{font-size:24px}.admin-panel{padding:14px}.admin-user{padding:10px}.actions-cell{gap:5px}.btn-sm{width:100%;justify-content:center;text-align:center}.admin-mini-item{align-items:stretch}.admin-log-top{flex-direction:column;align-items:flex-start}}
@media(max-width:768px){.dc-h-btn span:last-child{display:none}.dc-unread-badge{display:inline-flex!important;min-width:10px;height:10px;padding:0;font-size:0}}
::-webkit-scrollbar{width:6px}::-webkit-scrollbar-track{background:var(--bg)}::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}

/* ===== DIHCORD V1.5+ CUSTOMIZATION PATCH ===== */
:root{--chat-wallpaper:none;--chat-wallpaper-opacity:.22;--chat-motion-speed:1}
*{scroll-behavior:smooth}
.dc-main::before{content:'';position:absolute;inset:0;z-index:0;pointer-events:none;background-image:var(--chat-wallpaper);background-size:cover;background-position:center;opacity:var(--chat-wallpaper-opacity);filter:saturate(1.05) contrast(1.05)}
.dc-main>*{position:relative;z-index:1}.dc-msg-group,.dc-ch-item,.dc-nav-item,.dc-home-card,.forum-topic,.site-card,.pf-card,.profile-popup,.dc-input-shell,.btn{transition:transform calc(.18s * var(--chat-motion-speed)) ease,box-shadow calc(.24s * var(--chat-motion-speed)) ease,background calc(.22s * var(--chat-motion-speed)) ease,border-color calc(.22s * var(--chat-motion-speed)) ease,opacity calc(.2s * var(--chat-motion-speed)) ease}.dc-msg-group{animation:dcMsgIn calc(.22s * var(--chat-motion-speed)) ease both}.dc-ch-item:hover,.dc-nav-item:hover,.forum-topic:hover,.site-card:hover{transform:translateY(-1px)}@keyframes dcMsgIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}
.dc-md-h1{font-size:24px;font-weight:900;line-height:1.25;color:var(--t1);margin:8px 0 4px;letter-spacing:-.3px}.dc-md-h2{font-size:19px;font-weight:850;line-height:1.3;color:var(--t1);margin:7px 0 3px}.dc-md-line{min-height:1.35em}.dc-msg-text .dc-md-h1:first-child,.dc-msg-text .dc-md-h2:first-child{margin-top:0}
.pf-card{max-width:min(1120px,100%);border-radius:22px;box-shadow:0 24px 70px rgba(0,0,0,.28)}.pf-banner{height:220px;position:relative;overflow:hidden;background-size:200% 200%!important}.pp-banner{height:150px;position:relative;overflow:hidden;background-size:200% 200%!important}.pf-banner::after,.pp-banner::after{content:'';position:absolute;inset:-35%;background:linear-gradient(115deg,transparent 30%,rgba(255,255,255,.28) 48%,transparent 66%);transform:translateX(-50%);animation:bannerShine calc(5.5s * var(--chat-motion-speed)) ease-in-out infinite}.pf-theme-neon .pf-banner,.pf-theme-neon .pp-banner,.pf-theme-candy .pf-banner,.pf-theme-candy .pp-banner,.pf-theme-gold .pf-banner,.pf-theme-gold .pp-banner,.pf-theme-forest .pf-banner,.pf-theme-forest .pp-banner,.pf-theme-midnight .pf-banner,.pf-theme-midnight .pp-banner{animation:bannerFlow calc(8s * var(--chat-motion-speed)) ease-in-out infinite}.pf-banner.fx-slow,.pp-banner.fx-slow{animation:bannerFlow calc(12s * var(--chat-motion-speed)) ease-in-out infinite}.pf-banner.fx-pulse,.pp-banner.fx-pulse{animation:bannerPulse calc(3.2s * var(--chat-motion-speed)) ease-in-out infinite}.pf-banner.fx-shimmer::after,.pp-banner.fx-shimmer::after{animation-duration:calc(2.6s * var(--chat-motion-speed))}@keyframes bannerFlow{0%,100%{background-position:0% 50%}50%{background-position:100% 50%}}@keyframes bannerShine{0%,45%{transform:translateX(-70%) rotate(8deg);opacity:0}55%{opacity:.55}100%{transform:translateX(70%) rotate(8deg);opacity:0}}@keyframes bannerPulse{0%,100%{filter:saturate(1) brightness(1)}50%{filter:saturate(1.25) brightness(1.18)}}
.av-frame-neon .av-core,.av-frame-gold .av-core,.av-frame-ruby .av-core,.av-frame-emerald .av-core,.av-frame-frost .av-core{animation:avatarGlow calc(2.4s * var(--chat-motion-speed)) ease-in-out infinite}.av-frame-glitch .av-core{animation:avatarGlitch calc(1.8s * var(--chat-motion-speed)) steps(2,end) infinite}.av-shell.av-orbit::before{animation:avatarOrbit calc(6s * var(--chat-motion-speed)) linear infinite}.av-shell.av-sparkles::before,.av-shell.av-sparkles::after,.av-shell.av-confetti::before,.av-shell.av-confetti::after,.av-shell.av-bolts::before,.av-shell.av-bolts::after{animation:avatarFloat calc(2.1s * var(--chat-motion-speed)) ease-in-out infinite alternate}@keyframes avatarGlow{0%,100%{filter:brightness(1);transform:scale(1)}50%{filter:brightness(1.18);transform:scale(1.025)}}@keyframes avatarGlitch{0%,100%{transform:translate(0,0)}20%{transform:translate(1px,-1px)}40%{transform:translate(-1px,1px)}60%{transform:translate(1px,1px)}}@keyframes avatarOrbit{to{transform:rotate(360deg)}}@keyframes avatarFloat{from{transform:translateY(0) scale(1)}to{transform:translateY(-2px) scale(1.08)}}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation:none!important;transition:none!important;scroll-behavior:auto!important}}
@media(max-width:768px){.pf-banner{height:150px}.pp-banner{height:105px}.pf-card{border-radius:16px}}

</style>
</head>
<body class="dark-theme">
<div id="auth-screen" class="auth-screen"><div class="auth-bg"></div><div class="auth-card"><div class="auth-logo"><div class="auth-logo-icon">💬</div><div class="auth-logo-title">DIHCORD</div><div class="auth-logo-sub">School Chat • V1.5</div></div><div class="auth-tabs"><div class="auth-tab active" onclick="App.authTab('login')">LOG IN</div><div class="auth-tab" onclick="App.authTab('register')">REGISTER</div></div><div class="auth-field"><label class="auth-label">Username</label><input type="text" id="auth-user" class="auth-input" placeholder="your_username" autocomplete="off"></div><div class="auth-field"><label class="auth-label">Password</label><input type="password" id="auth-pass" class="auth-input" placeholder="••••••••"></div><button class="auth-btn" id="auth-btn" onclick="App.handleAuth()">LOG IN</button><div id="auth-error" class="auth-error"></div><div class="auth-footer">One account per computer • safer school mode</div></div></div>
<div id="app" class="app hidden"><div class="dc-channels"><div class="dc-ch-header"><span>💬</span><span>DIHCORD</span></div><div class="dc-server-card" id="dc-server-card"></div><div class="dc-search-shell"><input id="dc-channel-filter" class="dc-filter" type="text" placeholder="Search channels or DM..." oninput="App.setChannelFilter(this.value)"></div><div class="dc-cats" id="ch-list"></div><div class="dc-nav-shell collapsed" id="dc-nav-shell"><button class="dc-nav-toggle" id="dc-nav-toggle" onclick="App.toggleQuickNav()"><span>☰</span><span id="dc-nav-toggle-label" >Open Menu</span></button><div class="dc-nav-links" id="ch-nav"></div></div><div class="dc-user-panel" id="ch-user"></div></div><div class="dc-main" id="chat-area"><div class="dc-main-empty"><div class="dc-empty-icon">💬</div><div>Select a channel to start chatting</div></div></div><div class="dc-members hidden" id="dc-members"></div></div>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2/dist/umd/supabase.min.js"></script>
<script id="dih-core-script">
const SB_URL='https://ctdhcyvoptyqwjvmmiev.supabase.co',SB_KEY='eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImN0ZGhjeXZvcHR5cXdqdm1taWV2Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzQ4NDYwMjMsImV4cCI6MjA5MDQyMjAyM30.krkdrpL7scDp3-hvgcCcsZ23FJLchXavG5H1458PFEI';
const sb=window.supabase?.createClient?window.supabase.createClient(SB_URL,SB_KEY):null;
const EMOJIS=['👍','👎','❤️','🧡','💛','💚','💙','💜','😂','🤣','😊','😎','😮','😱','😢','😭','😡','🤔','🫡','😴','🔥','🎉','💀','✨','⭐','✅','❌','👀','🙌','👏','🙏','🤝','💯','⚡','🚀','🏆','🍕','🍪','🎮','🐱','🐶','🤖','🧠','📌','🔒','💬'];
const DIH_LOCK_SEAL='DIH-V15-LOCK-SEAL-20260414';
function fp(){let f=localStorage.getItem('chaty_fp');if(!f){f='fp_'+Date.now()+'_'+Math.random().toString(36).slice(2);localStorage.setItem('chaty_fp',f);}return f;}
function esc(t){return(t||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');}
function txt(v,f=''){const s=(v??'').toString().trim();return s||f;}
function initial(v,f='?'){return txt(v,f).charAt(0).toUpperCase()||f;}
function q(v){return JSON.stringify((v??'').toString());}
function attr(v){return(v??'').toString().replace(/&/g,'&amp;').replace(/"/g,'&quot;').replace(/</g,'&lt;').replace(/>/g,'&gt;');}
function randColor(){return'#'+Math.floor(Math.random()*0x1000000).toString(16).padStart(6,'0');}
function withTimeout(promise,ms,label='Request'){return Promise.race([promise,new Promise((_,reject)=>setTimeout(()=>reject(new Error(label+' timed out after '+ms+'ms')),ms))]);}
function sbReady(){return !!sb;}
function byDataId(id){return[...document.querySelectorAll('[data-id]')].find(el=>el.dataset.id===String(id))||null;}
function rc(t){const s=esc(t);return s.replace(/(https?:\/\/[^\s]+)/g,u=>{const c=u.replace(/&amp;/g,'&');if(/\.(gif|gifv|webp|png|jpg|jpeg)(\?.*)?$/i.test(c))return`<a href="${c}" target="_blank" rel="noopener noreferrer"><img class="dc-gif" src="${c.replace(/\.gifv/i,'.gif')}" loading="lazy"></a>`;if(/giphy\.com/i.test(c)){const m=c.match(/giphy\.com\/(?:gifs|media)\/(?:.*-)?([a-zA-Z0-9]+)/i);if(m)return`<a href="${c}" target="_blank" rel="noopener noreferrer"><img class="dc-gif" src="https://media.giphy.com/media/${m[1]}/giphy.gif" loading="lazy"></a>`;}if(/imgur\.com/i.test(c)){const m=c.match(/imgur\.com\/([a-zA-Z0-9]+)/i);if(m)return`<a href="${c}" target="_blank" rel="noopener noreferrer"><img class="dc-gif" src="https://i.imgur.com/${m[1]}.gif" loading="lazy"></a>`;}return`<a href="${c}" target="_blank" rel="noopener noreferrer" class="dc-link">${u}</a>`;});}
const stDot=s=>({online:'🟢',idle:'🌙',dnd:'⛔',invisible:'⚫'})[s||'online']||'🟢';
const META_OPEN='[[dih-meta]]';
const META_CLOSE='[[/dih-meta]]';
function parseUserMeta(rawBio){
  const source=String(rawBio||'');
  const match=source.match(/^\[\[dih-meta\]\](.*?)\[\[\/dih-meta\]\]\n?/s);
  let meta={prefix:'',avatar:'',decor:'none',avatarImg:'',frame:'none',theme:'default',statusNote:'',bio:source};
  if(!match)return meta;
  try{
    const parsed=JSON.parse(match[1]||'{}');
    meta.prefix=txt(parsed.prefix,'').slice(0,16);
    meta.avatar=txt(parsed.avatar,'').slice(0,4);
    meta.decor=txt(parsed.decor,'none').slice(0,16);
    meta.avatarImg=txt(parsed.avatarImg||parsed.avatarImage,'').slice(0,500);
    meta.frame=txt(parsed.frame,'none').slice(0,24);
    meta.theme=txt(parsed.theme,'default').slice(0,24);
    meta.statusNote=txt(parsed.statusNote,'').slice(0,64);
  }catch{}
  meta.bio=source.slice(match[0].length);
  return meta;
}
function buildUserBio(cleanBio,meta){
  const payload={prefix:txt(meta?.prefix,'').slice(0,16),avatar:txt(meta?.avatar,'').slice(0,4),decor:txt(meta?.decor,'none').slice(0,16),avatarImg:txt(meta?.avatarImg||meta?.avatarImage,'').slice(0,500),frame:txt(meta?.frame,'none').slice(0,24),theme:txt(meta?.theme,'default').slice(0,24),statusNote:txt(meta?.statusNote,'').slice(0,64)};
  const raw=JSON.stringify(payload);
  return `${META_OPEN}${raw}${META_CLOSE}\n${txt(cleanBio,'')}`.trim();
}
function userMeta(user){return parseUserMeta(user?.bio||'');}
function userPrefix(user){return userMeta(user).prefix;}
function userAvatarEmoji(user){return userMeta(user).avatar;}
function cleanAvatarDecor(value){
  const decor=txt(value,'none').toLowerCase();
  return['none','sparkles','crown','orbit','ribbon','laurel','pixel','confetti','halo','bolts','moon'].includes(decor)?decor:'none';
}
function userAvatarDecor(user){return cleanAvatarDecor(userMeta(user).decor);}
function cleanAvatarFrame(value){
  const frame=txt(value,'none').toLowerCase();
  return['none','neon','gold','ruby','emerald','frost','glitch'].includes(frame)?frame:'none';
}
function cleanProfileTheme(value){
  const theme=txt(value,'default').toLowerCase();
  return['default','neon','gold','candy','forest','midnight'].includes(theme)?theme:'default';
}
function userAvatarImage(user){return userMeta(user).avatarImg;}
function userAvatarFrame(user){return cleanAvatarFrame(userMeta(user).frame);}
function userProfileTheme(user){return cleanProfileTheme(userMeta(user).theme);}
function userStatusNote(user){return userMeta(user).statusNote;}
function userBioText(user){return userMeta(user).bio;}
function userDisplayName(user,fallback='user'){
  const base=txt(user?.display_name||user?.id,fallback);
  const prefix=userPrefix(user);
  return prefix?`[${prefix}] ${base}`:base;
}
function userAvatarGlyph(user,fallback='?'){
  const emoji=userAvatarEmoji(user);
  return emoji||initial(user?.display_name||user?.id,fallback);
}
function stripPrefixLabel(name){
  return txt(name,'').replace(/^\[[^\]]{1,16}\]\s*/,'').trim();
}
function parseMuteMeta(raw){
  const source=String(raw||'');
  const match=source.match(/^\[\[mute-until:(.*?)\]\](.*)$/s);
  if(!match)return{until:null,reason:source};
  const until=match[1]?new Date(match[1]):null;
  return{until:until&& !Number.isNaN(until.getTime())?until:null,reason:(match[2]||'').trim()};
}
function buildMuteReason(reason,untilIso=''){
  const clean=txt(reason,'').slice(0,120);
  return untilIso?`[[mute-until:${untilIso}]]${clean}`:clean;
}
function formatMuteReason(raw){
  const parsed=parseMuteMeta(raw);
  if(parsed.until)return `${parsed.reason||'Timed mute'} until ${parsed.until.toLocaleString()}`;
  return parsed.reason;
}
function parseForumTopic(raw){
  let source=String(raw||'').trim();
  let title='Untitled topic',tag='General',locked=false,pinned=false;
  const titleMatch=source.match(/^\[\[forum-title:(.*?)\]\]\n?/);
  if(titleMatch){title=txt(titleMatch[1],'Untitled topic').slice(0,80);source=source.slice(titleMatch[0].length);}
  const tagMatch=source.match(/^\[\[forum-tag:(.*?)\]\]\n?/);
  if(tagMatch){tag=txt(tagMatch[1],'General').slice(0,18);source=source.slice(tagMatch[0].length);}
  const lockMatch=source.match(/^\[\[forum-locked:(.*?)\]\]\n?/);
  if(lockMatch){locked=lockMatch[1]==='1';source=source.slice(lockMatch[0].length);}
  const pinMatch=source.match(/^\[\[forum-pinned:(.*?)\]\]\n?/);
  if(pinMatch){pinned=pinMatch[1]==='1';source=source.slice(pinMatch[0].length);}
  if(!titleMatch&&!tagMatch&&!lockMatch&&!pinMatch)return{title:source.slice(0,80)||'Untitled topic',body:source,tag:'General',locked:false,pinned:false};
  return{title,body:source.trim(),tag:tag||'General',locked,pinned};
}
function buildForumTopic(title,body,meta={}){
  const parts=[
    `[[forum-title:${txt(title,'Untitled topic').slice(0,80)}]]`,
    `[[forum-tag:${txt(meta.tag,'General').slice(0,18)}]]`
  ];
  if(meta.locked)parts.push('[[forum-locked:1]]');
  if(meta.pinned)parts.push('[[forum-pinned:1]]');
  return `${parts.join('\n')}\n${txt(body,'').trim()}`.trim();
}
function parsePollContent(raw){
  const source=String(raw||'').trim();
  const match=source.match(/^\[\[poll\]\](\{[\s\S]*\})$/);
  if(!match)return null;
  try{
    const parsed=JSON.parse(match[1]);
    const question=txt(parsed.question,'Poll');
    const options=(Array.isArray(parsed.options)?parsed.options:[]).map(v=>txt(v,'')).filter(Boolean).slice(0,8);
    if(question&&options.length>=2)return{question,options,closed:!!parsed.closed};
  }catch{}
  return null;
}
function buildPollContent(question,options,meta={}){
  return `[[poll]]${JSON.stringify({question:txt(question,'Poll').slice(0,120),options:(options||[]).map(v=>txt(v,'').slice(0,40)).filter(Boolean).slice(0,8),closed:!!meta.closed})}`;
}
function mentionCandidates(user){
  const raw=[user?.id,user?.display_name,stripPrefixLabel(user?.display_name||'')];
  return [...new Set(raw.map(v=>txt(v,'').toLowerCase()).filter(v=>/^[a-z0-9_-]{2,24}$/.test(v)))];
}
function parseSiteLockReason(raw){
  const source=String(raw||'').trim();
  const match=source.match(/^\[\[site-lock\]\](\{[\s\S]*\})$/);
  if(!match)return{code:'custom',label:'Temporary lock',note:source};
  try{
    const parsed=JSON.parse(match[1]||'{}');
    return{code:txt(parsed.code,'custom'),label:txt(parsed.label,'Temporary lock'),note:txt(parsed.note,'')};
  }catch{}
  return{code:'custom',label:'Temporary lock',note:source};
}
function buildSiteLockReason(code,label,note=''){
  return `[[site-lock]]${JSON.stringify({code:txt(code,'custom').slice(0,24),label:txt(label,'Temporary lock').slice(0,48),note:txt(note,'').slice(0,180)})}`;
}
function parseHomeNews(raw){
  const source=String(raw||'').trim();
  const fallback={version:'V20.3',title:'DIHCORD Updates',body:'Welcome to the latest DIHCORD build.',tone:'info'};
  const match=source.match(/^\[\[home-news\]\](\{[\s\S]*\})$/);
  if(!match)return{...fallback,body:source||fallback.body};
  try{
    const parsed=JSON.parse(match[1]||'{}');
    return{
      version:txt(parsed.version,fallback.version).slice(0,32),
      title:txt(parsed.title,fallback.title).slice(0,80),
      body:txt(parsed.body,fallback.body).slice(0,420),
      tone:['info','good','warn','hot'].includes(txt(parsed.tone,'info'))?txt(parsed.tone,'info'):'info'
    };
  }catch{}
  return fallback;
}
function buildHomeNews(version,title,body,tone='info'){
  return `[[home-news]]${JSON.stringify({version:txt(version,'V20.3').slice(0,32),title:txt(title,'DIHCORD Updates').slice(0,80),body:txt(body,'').slice(0,420),tone:['info','good','warn','hot'].includes(tone)?tone:'info'})}`;
}
function parseImageContent(raw){
  const source=String(raw||'').trim();
  const match=source.match(/^\[\[image\]\](\{[\s\S]*\})$/);
  if(!match)return null;
  try{
    const parsed=JSON.parse(match[1]||'{}');
    const src=txt(parsed.src,'');
    if(!src)return null;
    return{src,name:txt(parsed.name,'image'),caption:txt(parsed.caption,''),mime:txt(parsed.mime,''),mode:txt(parsed.mode,'')};
  }catch{}
  return null;
}
function buildImageContent(payload){
  return `[[image]]${JSON.stringify({src:txt(payload?.src,''),name:txt(payload?.name,'image').slice(0,120),caption:txt(payload?.caption,'').slice(0,500),mime:txt(payload?.mime,'').slice(0,80),mode:txt(payload?.mode,'').slice(0,24)})}`;
}

const App={
  mode:'login',ch:null,replyTo:null,page:'home',_sub:null,_tsub:null,_inboxSub:null,_systemSub:null,_session:null,_role:'user',_me:null,_cache:{},_audioCtx:null,_typingTimer:null,_toastTimer:null,_forumTopicId:null,_msgPageSize:60,_oldestMsgAt:null,_loadedAllHistory:false,_loadingHistory:false,_maxMessageLength:500,_windowMs:15000,_rateLimit:5,_burstMs:4000,_burstLimit:3,_minSendGapMs:900,_recentSends:[],_lastSendAt:0,_cooldownUntil:0,_authKey:'chaty_auth_guard',_maxNameLength:24,_maxPasswordLength:64,_maxBioLength:180,_maxPrefixLength:16,_maxChannelNameLength:24,_maxChannelDescLength:120,_channelFilter:'',_memberFilter:'',_lastUsers:[],_lastChannels:[],_dmMeta:{},_themeKey:'dih_theme_pref',_navKey:'dih_nav_expanded',_favoritesKey:'dih_fav_channels_v1',_unreadKey:'dih_unread_dm_v2',_inboxKey:'dih_inbox_v1',_settingsKey:'dih_site_settings_v1',_draftsKey:'dih_channel_drafts_v1',_savedKey:'dih_saved_messages_v1',_mutedChannelsKey:'dih_muted_channels_v1',_titleBase:'DIHCORD - V1.5',_unread:{},_favorites:{},_inboxItems:[],_drafts:{},_savedMessages:[],_mutedChannels:{},_settings:{sounds:true,desktopNotices:true,dmPreviews:true},_visibilityHooked:false,_theme:'dark',_navExpanded:false,_siteLock:null,_homeNews:{version:'V20.3',title:'DIHCORD V20.3',body:'Discord-style profiles, avatar photos, frames and safer chat tools are live.',tone:'info',updatedAt:null,modId:'system'},_siteLockOwnerId:'mrkotyvell',_pendingUpload:null,_uploadBucket:'chaty-media',_maxUploadBytes:3*1024*1024,_maxGifUploadBytes:2*1024*1024,_blockedWords:['porn','nudes','doxx','swat','gore'],_riskyDomains:['grabify','iplogger','discord.gift','bit.ly','tinyurl.com'],_loadingChs:false,_queuedLoadChs:false,_lastLoadChsAt:0,_loadChsTimer:null,_chatRefreshTimer:null,_forumRefreshTimer:null,_userRefreshTimer:null,_typingPollMs:8000,_lastTypingRefreshAt:0,_maxRenderedMessages:90,_liveTrafficWindowMs:4000,_liveTrafficLimit:18,_liveTrafficSuspendMs:15000,_liveTrafficHits:[],_liveTrafficUntil:0,_liveTrafficDropped:0,_liveTrafficTimer:null,_adminRefreshing:false,

  init(){this._hydrateUiPrefs();this._hydrateUnread();this._hydrateInbox();this._bindWindowState();if(sbReady()){this._setupSystemSub();this._refreshSiteLockState();}const s=localStorage.getItem('chaty_session');if(s&&sbReady()){try{this._session=JSON.parse(s);this.showApp();return;}catch{}}this.showAuth();if(!sbReady())document.getElementById('auth-error').textContent='Supabase failed to load. Check internet or CDN access, then refresh.';},
  _dbMsg(){return'Supabase is unavailable. Refresh the page and try again.';},
  _hydrateUnread(){
    try{this._unread=JSON.parse(localStorage.getItem(this._unreadKey)||'{}')||{};}
    catch{this._unread={};}
    this._updateTitle();
  },
  _persistUnread(){localStorage.setItem(this._unreadKey,JSON.stringify(this._unread));this._updateTitle();},
  _hydrateInbox(){
    try{this._inboxItems=JSON.parse(localStorage.getItem(this._inboxKey)||'[]')||[];}
    catch{this._inboxItems=[];}
  },
  _persistInbox(){
    localStorage.setItem(this._inboxKey,JSON.stringify((this._inboxItems||[]).slice(0,100)));
    this._renderNav();
  },
  _inboxUnreadCount(){return (this._inboxItems||[]).filter(item=>!item.read).length;},
  _addInboxItem(item){
    const entry={id:'ibox_'+Date.now()+'_'+Math.random().toString(36).slice(2,8),read:false,ts:Date.now(),type:'notice',title:'Update',body:'',channelId:null,topicId:null,...item};
    this._inboxItems=[entry,...(this._inboxItems||[])].slice(0,100);
    this._persistInbox();
  },
  _markInboxItemRead(id){
    this._inboxItems=(this._inboxItems||[]).map(item=>item.id===id?{...item,read:true}:item);
    this._persistInbox();
  },
  _markAllInboxRead(){
    this._inboxItems=(this._inboxItems||[]).map(item=>({...item,read:true}));
    this._persistInbox();
  },
  _hydrateFavorites(){
    try{this._favorites=JSON.parse(localStorage.getItem(this._favoritesKey)||'{}')||{};}
    catch{this._favorites={};}
  },
  _persistFavorites(){localStorage.setItem(this._favoritesKey,JSON.stringify(this._favorites||{}));},
  _hydrateSettings(){
    const defaults={sounds:true,desktopNotices:true,dmPreviews:true};
    try{this._settings={...defaults,...(JSON.parse(localStorage.getItem(this._settingsKey)||'{}')||{})};}
    catch{this._settings=defaults;}
  },
  _persistSettings(){localStorage.setItem(this._settingsKey,JSON.stringify(this._settings||{}));},
  _hydrateDrafts(){
    try{this._drafts=JSON.parse(localStorage.getItem(this._draftsKey)||'{}')||{};}
    catch{this._drafts={};}
  },
  _persistDrafts(){localStorage.setItem(this._draftsKey,JSON.stringify(this._drafts||{}));},
  _draftFor(id){return txt(this._drafts?.[id],'');},
  _setDraft(id,text=''){
    if(!id)return;
    const clean=String(text||'').slice(0,this._maxMessageLength);
    if(clean)this._drafts[id]=clean;
    else delete this._drafts[id];
    this._persistDrafts();
  },
  _clearDraft(id){
    if(!id||!this._drafts?.[id])return;
    delete this._drafts[id];
    this._persistDrafts();
  },
  _draftCount(){return Object.keys(this._drafts||{}).length;},
  clearAllDrafts(){
    if(!this._draftCount()||!confirm('Clear all saved drafts on this device?'))return;
    this._drafts={};
    this._persistDrafts();
    const input=document.getElementById('chat-input');
    if(this.page==='chat'&&input&&!input.disabled){
      input.value='';
      this._updateComposerMeta();
    }
    if(this.page==='settings')this.goSettings();
  },
  _hydrateSavedMessages(){
    try{this._savedMessages=JSON.parse(localStorage.getItem(this._savedKey)||'[]')||[];}
    catch{this._savedMessages=[];}
  },
  _persistSavedMessages(){
    localStorage.setItem(this._savedKey,JSON.stringify((this._savedMessages||[]).slice(0,150)));
    this._renderNav();
  },
  _isSavedMessage(id){return (this._savedMessages||[]).some(item=>String(item.id)===String(id));},
  _savedCount(){return (this._savedMessages||[]).length;},
  _snapshotSavedMessage(msg){
    const channel=(this._lastChannels||[]).find(c=>c.id===msg.channel_id);
    const topicId=channel?.type==='forum'?(msg.reply_to||msg.id):'';
    return{
      id:String(msg.id),
      channelId:msg.channel_id||'',
      channelName:channel?.name||msg.channel_id||'channel',
      channelType:channel?.type||'public',
      topicId:String(topicId||''),
      author:msg.user_name||msg.user_id||'user',
      preview:this._messagePreview(msg,180),
      content:String(msg.content||''),
      createdAt:msg.created_at||new Date().toISOString(),
      savedAt:Date.now()
    };
  },
  _removeSavedMessage(id,rerender=true){
    this._savedMessages=(this._savedMessages||[]).filter(item=>String(item.id)!==String(id));
    this._persistSavedMessages();
    if(rerender&&this.page==='saved')this.goSaved();
  },
  _clearSavedMessages(){
    if(!this._savedCount()||!confirm('Clear all saved messages on this device?'))return;
    this._savedMessages=[];
    this._persistSavedMessages();
    if(this.page==='saved')this.goSaved();
  },
  async toggleSavedMessage(id){
    if(this._isSavedMessage(id)){
      this._removeSavedMessage(id,false);
      if(this.page==='chat')this._scheduleChatRefresh(80);
      if(this.page==='saved')this.goSaved();
      return;
    }
    if(!this._requireDb())return;
    const {data:msg,error}=await sb.from('chaty_messages').select('id,channel_id,user_id,user_name,content,platform,reply_to,reactions,pinned,edited,created_at').eq('id',id).single();
    if(error||!msg){alert(error?.message||'Message not found.');return;}
    const item=this._snapshotSavedMessage(msg);
    this._savedMessages=[item,...(this._savedMessages||[]).filter(entry=>String(entry.id)!==String(item.id))].slice(0,150);
    this._persistSavedMessages();
    if(this.page==='chat')this._scheduleChatRefresh(80);
  },
  openSavedItem(id){
    const item=(this._savedMessages||[]).find(entry=>String(entry.id)===String(id));
    if(!item)return;
    if(item.topicId)this._forumTopicId=item.topicId;
    this.openChat(item.channelId);
  },
  _hydrateMutedChannels(){
    try{this._mutedChannels=JSON.parse(localStorage.getItem(this._mutedChannelsKey)||'{}')||{};}
    catch{this._mutedChannels={};}
  },
  _persistMutedChannels(){localStorage.setItem(this._mutedChannelsKey,JSON.stringify(this._mutedChannels||{}));},
  _isChannelMuted(id){return !!this._mutedChannels?.[id];},
  toggleChannelMute(id){
    if(!id)return;
    if(this._isChannelMuted(id))delete this._mutedChannels[id];
    else this._mutedChannels[id]=1;
    this._persistMutedChannels();
    if(this.page==='chat'&&this.ch===id)this.openChat(id);
    else{
      this._scheduleLoadChs(120);
      if(this.page==='settings')this.goSettings();
    }
  },
  isPrimaryOwner(){return this._session?.id===this._siteLockOwnerId;},
  _siteLockOptions(){
    return[
      {value:'technical',label:'Technical maintenance'},
      {value:'database',label:'Database update'},
      {value:'security',label:'Security review'},
      {value:'emergency',label:'Emergency fix'},
      {value:'cleanup',label:'Server cleanup'},
      {value:'custom',label:'Custom reason'}
    ];
  },
  _siteLockLabel(code){
    return this._siteLockOptions().find(item=>item.value===code)?.label||'Temporary lock';
  },
  async _loadSiteLockState(){
    if(!sbReady())return null;
    const {data}=await sb.from('chaty_mod_log').select('action,reason,created_at,mod_id').in('action',['SITE_LOCK','SITE_UNLOCK']).order('created_at',{ascending:false}).limit(1);
    const latest=data?.[0];
    if(!latest||latest.action==='SITE_UNLOCK'){this._siteLock={active:false};return this._siteLock;}
    const parsed=parseSiteLockReason(latest.reason);
    this._siteLock={active:true,code:parsed.code,label:parsed.label,note:parsed.note,modId:latest.mod_id||this._siteLockOwnerId,createdAt:latest.created_at};
    return this._siteLock;
  },
  async _loadHomeNewsState(){
    if(!sbReady())return this._homeNews;
    const {data}=await sb.from('chaty_mod_log').select('reason,created_at,mod_id').eq('action','HOME_NEWS_UPDATE').order('created_at',{ascending:false}).limit(1);
    const latest=data?.[0];
    if(!latest)return this._homeNews;
    const parsed=parseHomeNews(latest.reason);
    this._homeNews={...parsed,updatedAt:latest.created_at,modId:latest.mod_id||this._siteLockOwnerId};
    return this._homeNews;
  },
  async _refreshHomeNewsState(){
    await this._loadHomeNewsState();
    if(this.page==='home')this.goHome();
    if(this.page==='admin'&&this.isPrimaryOwner()&&!this._adminRefreshing)this.goAdmin();
  },
  async _refreshSiteLockState(){
    await this._loadSiteLockState();
    this._applySiteLockState();
    if(this.page==='admin'&&this.isPrimaryOwner()&&!this._adminRefreshing)this.goAdmin();
  },
  _applySiteLockState(){
    const active=!!this._siteLock?.active;
    const bypass=this.isPrimaryOwner();
    let overlay=document.getElementById('site-lock-screen');
    if(!active||bypass){
      overlay?.remove();
      document.body.classList.remove('site-locked');
      return;
    }
    document.body.classList.add('site-locked');
    if(!overlay){
      overlay=document.createElement('div');
      overlay.id='site-lock-screen';
      overlay.className='site-lock-screen';
      document.body.appendChild(overlay);
    }
    const label=esc(this._siteLock?.label||'Temporary lock');
    const note=esc(this._siteLock?.note||'The website is paused right now. Please wait until the owner opens it again.');
    const when=this._siteLock?.createdAt?new Date(this._siteLock.createdAt).toLocaleString():'now';
    const by=esc(this._siteLock?.modId||this._siteLockOwnerId);
    overlay.innerHTML=`<div class="site-lock-card"><div class="site-lock-kicker">Live Website Lock</div><div class="site-lock-title">Website Temporarily Paused</div><div class="site-lock-text">This DIHCORD session was blocked by the owner and updated live for everyone without a reload. Please wait until access is restored.</div><div class="site-lock-reason"><div class="site-lock-label">${label}</div><div class="site-lock-note">${note}</div></div><div class="site-lock-meta">Updated by @${by} • ${esc(when)}</div></div>`;
  },
  _setupSystemSub(){
    if(!sbReady())return;
    if(this._systemSub)sb.removeChannel(this._systemSub);
    this._systemSub=sb.channel('site-lock-global').on('postgres_changes',{event:'INSERT',schema:'public',table:'chaty_mod_log'},payload=>{
      const action=payload?.new?.action;
      if(action==='SITE_LOCK'||action==='SITE_UNLOCK')this._refreshSiteLockState();
      if(action==='HOME_NEWS_UPDATE')this._refreshHomeNewsState();
    }).on('postgres_changes',{event:'*',schema:'public',table:'chaty_users'},payload=>this._scheduleUserCacheRefresh(payload?.new?.id||payload?.old?.id)).subscribe();
  },
  _scheduleUserCacheRefresh(uid=''){
    clearTimeout(this._userRefreshTimer);
    this._userRefreshTimer=setTimeout(()=>this._refreshUserCache(uid),450);
  },
  async _refreshUserCache(uid=''){
    if(!this._requireDb(false))return;
    let users=[];
    if(uid){
      const {data}=await sb.from('chaty_users').select('id,display_name,avatar_color,role,banned,muted,mute_reason,user_status,bio,warnings,created_at').eq('id',uid);
      users=data||[];
    }else{
      const {data}=await sb.from('chaty_users').select('id,display_name,avatar_color,role,banned,muted,mute_reason,user_status,bio,warnings,created_at');
      users=data||[];
      this._lastUsers=users;
    }
    for(const user of users){
      this._cache[user.id]=user;
      if(this._me?.id===user.id){
        this._me={...this._me,...user};
        this._role=user.role||this._role||'user';
        this._session.role=this._role;
        localStorage.setItem('chaty_session',JSON.stringify(this._session));
        this._renderNav();
        this._syncNavShell();
        this._renderUserPanel(this._me);
      }
    }
    if(uid)this._lastUsers=(this._lastUsers||[]).map(u=>u.id===uid?{...u,...(this._cache[uid]||{})}:u);
    if(this.page==='chat'&&this.ch)this._scheduleChatRefresh(220);
    if(this.page==='home')this.goHome();
    this._scheduleLoadChs(500);
  },
  async _cacheUserById(uid){
    if(!uid||this._cache?.[uid]||!this._requireDb(false))return this._cache?.[uid]||null;
    const {data:user}=await sb.from('chaty_users').select('id,display_name,avatar_color,role,banned,muted,mute_reason,user_status,bio,warnings,created_at').eq('id',uid).single();
    if(user){
      this._cache[user.id]=user;
      if(!this._lastUsers.some(u=>u.id===user.id))this._lastUsers=[...(this._lastUsers||[]),user];
    }
    return user||null;
  },
  _siteLockCardHtml(){
    const current=this._siteLock?.active?this._siteLock:{active:false,code:'technical',label:'Technical maintenance',note:''};
    const options=this._siteLockOptions().map(item=>`<option value="${item.value}" ${current.code===item.value?'selected':''}>${esc(item.label)}</option>`).join('');
    const state=current.active?`<div class="admin-msg error">Live now: ${esc(current.label||'Temporary lock')} • ${esc(current.note||'No note')} • ${esc(current.createdAt?new Date(current.createdAt).toLocaleString():'now')}</div>`:`<div class="admin-msg success">Website is open right now.</div>`;
    return `<div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Website Lock</div><div class="admin-card-sub">Visible only to @mrkotyvell</div></div></div><div class="site-lock-admin-note">This control blocks the whole website for everyone except your account, and it pushes live to open screens without a reload.</div>${state}<div class="form-block" style="margin-top:16px"><div class="form-grid"><div><label class="form-label">Reason</label><select id="site-lock-reason" class="form-input" onchange="App.toggleSiteLockCustom()">${options}</select></div><div><label class="form-label">Quick Note</label><input type="text" id="site-lock-note" class="form-input" maxlength="180" value="${attr(current.note||'')}" placeholder="Short message users will see"></div></div><div id="site-lock-custom-wrap" class="${(current.code||'technical')==='custom'?'':'hidden'}" style="margin-top:12px"><label class="form-label">Custom Reason Title</label><input type="text" id="site-lock-custom-title" class="form-input" maxlength="48" value="${attr((current.code||'')==='custom'?(current.label||''):'')}" placeholder="Custom reason title"></div><div class="site-actions" style="margin-top:14px"><button class="btn btn-red" onclick="App.applySiteLock()">Apply Lock</button><button class="btn btn-outline" onclick="App.clearSiteLock()">Unlock Site</button></div><div id="site-lock-msg" class="admin-msg"></div></div></div>`;
  },
  _homeNewsCardHtml(){
    const news=this._homeNews||parseHomeNews('');
    const toneOptions=['info','good','warn','hot'].map(t=>`<option value="${t}" ${news.tone===t?'selected':''}>${t.toUpperCase()}</option>`).join('');
    const when=news.updatedAt?new Date(news.updatedAt).toLocaleString():'not published yet';
    return `<div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Home News & Current Version</div><div class="admin-card-sub">Only @mrkotyvell can publish this to everyone</div></div></div><div class="site-lock-admin-note">This controls the news card on the Home panel for every open client. It updates live through realtime without a reload.</div><div class="admin-msg success">Current Home: ${esc(news.version||'V20.3')} • ${esc(news.title||'DIHCORD Updates')} • ${esc(when)}</div><div class="form-block" style="margin-top:16px"><div class="form-grid"><div><label class="form-label">Current Version</label><input type="text" id="home-news-version" class="form-input" maxlength="32" value="${attr(news.version||'V20.3')}" placeholder="V20.3"></div><div><label class="form-label">Tone</label><select id="home-news-tone" class="form-input">${toneOptions}</select></div><div><label class="form-label">News Title</label><input type="text" id="home-news-title" class="form-input" maxlength="80" value="${attr(news.title||'DIHCORD Updates')}" placeholder="What changed?"></div></div><label class="form-label" style="margin-top:12px">News Body</label><textarea id="home-news-body" class="form-input form-textarea" maxlength="420" placeholder="Tell everyone what is new...">${esc(news.body||'')}</textarea><div class="site-actions" style="margin-top:14px"><button class="btn btn-accent" onclick="App.applyHomeNews()">Publish News</button><button class="btn btn-outline" onclick="App.previewHomeNews()">Preview Home</button></div><div id="home-news-msg" class="admin-msg"></div></div></div>`;
  },
  previewHomeNews(){
    const version=(document.getElementById('home-news-version')?.value||'V20.3').trim();
    const title=(document.getElementById('home-news-title')?.value||'DIHCORD Updates').trim();
    const body=(document.getElementById('home-news-body')?.value||'').trim();
    const tone=(document.getElementById('home-news-tone')?.value||'info').trim();
    this._homeNews={version,title,body,tone,updatedAt:new Date().toISOString(),modId:this._session?.id||this._siteLockOwnerId};
    this.goHome();
  },
  async applyHomeNews(){
    if(!this._requireDb()||!this.isPrimaryOwner())return;
    const msg=document.getElementById('home-news-msg');
    const version=(document.getElementById('home-news-version')?.value||'V20.3').trim().slice(0,32);
    const title=(document.getElementById('home-news-title')?.value||'DIHCORD Updates').trim().slice(0,80);
    const body=(document.getElementById('home-news-body')?.value||'').trim().slice(0,420);
    const tone=(document.getElementById('home-news-tone')?.value||'info').trim();
    const reason=buildHomeNews(version,title,body||'No details yet.',tone);
    const {error}=await sb.from('chaty_mod_log').insert({action:'HOME_NEWS_UPDATE',target_id:'home',mod_id:this._session.id,reason});
    if(msg){
      msg.textContent=error?error.message:'Home news published live for everyone.';
      msg.className='admin-msg '+(error?'error':'success');
    }
    if(!error)await this._refreshHomeNewsState();
  },
  toggleSiteLockCustom(){
    document.getElementById('site-lock-custom-wrap')?.classList.toggle('hidden',(document.getElementById('site-lock-reason')?.value||'technical')!=='custom');
  },
  async applySiteLock(){
    if(!this._requireDb()||!this.isPrimaryOwner())return;
    const msg=document.getElementById('site-lock-msg');
    const code=(document.getElementById('site-lock-reason')?.value||'technical').trim();
    const note=(document.getElementById('site-lock-note')?.value||'').trim().slice(0,180);
    const customTitle=(document.getElementById('site-lock-custom-title')?.value||'').trim().slice(0,48);
    const label=code==='custom'?(customTitle||'Custom reason'):this._siteLockLabel(code);
    const reason=buildSiteLockReason(code,label,note||`Paused by @${this._siteLockOwnerId}. Please try again soon.`);
    const {error}=await sb.from('chaty_mod_log').insert({action:'SITE_LOCK',target_id:'global',mod_id:this._session.id,reason});
    if(msg){
      msg.textContent=error?error.message:'Website lock applied live.';
      msg.className='admin-msg '+(error?'error':'success');
    }
    if(!error)await this._refreshSiteLockState();
  },
  async clearSiteLock(){
    if(!this._requireDb()||!this.isPrimaryOwner())return;
    const msg=document.getElementById('site-lock-msg');
    const {error}=await sb.from('chaty_mod_log').insert({action:'SITE_UNLOCK',target_id:'global',mod_id:this._session.id,reason:'Website reopened'});
    if(msg){
      msg.textContent=error?error.message:'Website unlocked live.';
      msg.className='admin-msg '+(error?'error':'success');
    }
    if(!error)await this._refreshSiteLockState();
  },
  _unreadCount(id){return Math.max(0,Number(this._unread?.[id]||0));},
  _totalUnread(){return Object.values(this._unread||{}).reduce((sum,val)=>sum+Math.max(0,Number(val)||0),0);},
  _updateTitle(){document.title=this._totalUnread()?`(${this._totalUnread()}) ${this._titleBase}`:this._titleBase;},
  _markRead(id){if(!id||!this._unread[id])return;delete this._unread[id];this._persistUnread();},
  _bumpUnread(id){if(!id)return;this._unread[id]=this._unreadCount(id)+1;this._persistUnread();},
  _renderNav(){
    const inboxBadge=this._inboxUnreadCount()?`<span class="nav-badge">${this._inboxUnreadCount()>99?'99+':this._inboxUnreadCount()}</span>`:'';
    const savedBadge=this._savedCount()?`<span class="nav-badge">${this._savedCount()>99?'99+':this._savedCount()}</span>`:'';
    const staff=this.isStaff();
    let nav=`<div class="dc-nav-item" id="nav-home" onclick="App.goHome()"><span>🏠</span><span>Home</span></div><div class="dc-nav-item" id="nav-inbox" onclick="App.goInbox()"><span>🔔</span><span>Inbox</span>${inboxBadge}</div><div class="dc-nav-item" id="nav-saved" onclick="App.goSaved()"><span>SV</span><span>Saved</span>${savedBadge}</div><div class="dc-nav-item" id="nav-profile" onclick="App.goProfile()"><span>👤</span><span>My Profile</span></div><div class="dc-nav-item" id="nav-settings" onclick="App.goSettings()"><span>🧰</span><span>Settings</span></div>`;
    if(staff)nav+=`<div class="dc-nav-item" id="nav-admin" onclick="App.goAdmin()"><span>⚙️</span><span>Admin</span></div>`;
    const mount=document.getElementById('ch-nav');
    if(mount){
      mount.innerHTML=nav;
      const activeMap={home:'nav-home',inbox:'nav-inbox',saved:'nav-saved',profile:'nav-profile',settings:'nav-settings',admin:'nav-admin'};
      document.getElementById(activeMap[this.page]||'')?.classList.add('dc-active');
    }
  },
  _isFavorite(id){return !!this._favorites?.[id];},
  toggleFavorite(id){
    if(!id)return;
    if(this._isFavorite(id))delete this._favorites[id];
    else this._favorites[id]=1;
    this._persistFavorites();
    this.loadChs();
    const btn=document.getElementById('dc-fav-btn');
    if(btn&&this.ch===id){
      btn.classList.toggle('active',this._isFavorite(id));
      btn.title=this._isFavorite(id)?'Remove from favorites':'Add to favorites';
      const label=btn.querySelector('span:last-child');
      if(label)label.textContent=this._isFavorite(id)?'Starred':'Star';
    }
    if(this.page==='home')this.goHome();
  },
  _textSnippet(text,max=42){
    const clean=String(text||'').replace(/\s+/g,' ').trim();
    if(!clean)return 'No messages yet';
    return clean.length>max?`${clean.slice(0,max-1)}...`:clean;
  },
  _relativeTime(ts){
    if(!ts)return '';
    const diff=Math.max(0,Date.now()-Number(ts));
    const min=60000,hour=3600000,day=86400000;
    if(diff<min)return 'now';
    if(diff<hour)return `${Math.floor(diff/min)}m`;
    if(diff<day)return `${Math.floor(diff/hour)}h`;
    if(diff<day*7)return `${Math.floor(diff/day)}d`;
    return new Date(ts).toLocaleDateString();
  },
  _isRetiredBridgeChannel(channel){
    return channel?.id==='alyon-bridge'||channel?.type==='bridge';
  },
  _channelGlyph(channel){
    if(this._isRetiredBridgeChannel(channel))return '#';
    if(channel?.id==='votes')return '🗳️';
    if(channel?.type==='dm')return '@';
    if(channel?.type==='mod')return '🛡';
    if(channel?.type==='forum')return '🧵';
    return '#';
  },
  _channelLabel(channelId){
    const channel=(this._lastChannels||[]).find(c=>c.id===channelId);
    if(!channel)return String(channelId||'channel');
    if(channel.type==='dm'){
      const otherId=(channel.members||[]).find(m=>m!==this._session?.id);
      const user=this._cache[otherId];
      return this._displayName(user||{id:otherId,display_name:otherId},otherId||'DM');
    }
    return String(channel.name||channel.id).replace(/^#\s*/,'');
  },
  _favoriteChannels(){
    return (this._lastChannels||[]).filter(c=>c.id!=='votes'&&this._isFavorite(c.id)&&!this._isRetiredBridgeChannel(c)&&c.type!=='dm'&&(c.type!=='mod'||this.isStaff()));
  },
  _recentDmChannels(limit=5){
    return (this._lastChannels||[]).filter(c=>c.type==='dm'&&(c.members||[]).includes(this._session?.id)).sort((a,b)=>(this._dmMeta[b.id]?.ts||0)-(this._dmMeta[a.id]?.ts||0)).slice(0,limit);
  },
  _forumTopicMeta(msg){
    const parsed=parseForumTopic(msg?.content||'');
    return{
      title:parsed.title||'Untitled topic',
      body:parsed.body||'',
      tag:parsed.tag||'General',
      locked:!!parsed.locked,
      pinned:!!parsed.pinned,
      preview:this._textSnippet(parsed.body||parsed.title||'',120)
    };
  },
  _forumReplies(allMsgs,topicId){
    return (allMsgs||[]).filter(msg=>String(msg.reply_to||'')===String(topicId)).sort((a,b)=>new Date(a.created_at)-new Date(b.created_at));
  },
  async _openForum(ch){
    const area=document.getElementById('chat-area');
    const safeName=esc((ch?.name||'# forum').replace(/^#\s*/,''));
    const safeDesc=esc(ch?.description||'Forum');
    this._closeLiveSubs();
    document.getElementById('dc-members')?.classList.add('hidden');
    area.innerHTML=`<div class="dc-header"><span class="dc-h-icon">🧵</span><span class="dc-h-name">${safeName}</span><span class="dc-h-tag">FORUM</span><span style="color:var(--border);margin:0 6px">|</span><span class="dc-h-desc">${safeDesc}</span><div class="dc-h-actions"><button class="dc-h-btn ${this._isFavorite(ch.id)?'active':''}" id="dc-fav-btn" onclick='App.toggleFavorite(${q(ch.id)})'><span>★</span><span>${this._isFavorite(ch.id)?'Starred':'Star'}</span></button><button class="dc-h-btn" onclick="App.showSearchPanel()"><span>🔎</span><span>Search</span></button></div></div><div class="forum-shell" id="forum-shell"><div class="forum-empty">Loading forum...</div></div>`;
    let topics,error;
    try{
      ({data:topics,error}=await withTimeout(sb.from('chaty_messages').select('id,channel_id,user_id,user_name,content,platform,reply_to,reactions,pinned,edited,created_at').eq('channel_id',ch.id).order('created_at',{ascending:false}).limit(150),8000,'Loading forum'));
    }catch(e){
      error={message:e.message};
    }
    if(error){document.getElementById('forum-shell').innerHTML=`<div class="forum-empty">${esc(error.message||'Failed to load forum')}</div>`;return;}
    const all=topics||[];
    const roots=all.filter(msg=>!msg.reply_to).sort((a,b)=>{
      const aMeta=this._forumTopicMeta(a),bMeta=this._forumTopicMeta(b);
      if(!!bMeta.pinned!==!!aMeta.pinned)return Number(bMeta.pinned)-Number(aMeta.pinned);
      return new Date(b.created_at)-new Date(a.created_at);
    });
    if(!this._forumTopicId||!roots.some(msg=>String(msg.id)===String(this._forumTopicId)))this._forumTopicId=roots[0]?.id||null;
    const active=roots.find(msg=>String(msg.id)===String(this._forumTopicId))||null;
    const activeMeta=active?this._forumTopicMeta(active):null;
    const replies=active?this._forumReplies(all,active.id):[];
    const replyLocked=!!activeMeta?.locked&&!this.isStaff();
    document.getElementById('forum-shell').innerHTML=`<div class="forum-hero"><div class="forum-title">Forum Department</div><div class="forum-sub">Longer discussions, ideas, feedback and school threads live here. Start a topic, then let people reply under it.</div></div><div class="forum-grid"><div class="forum-col"><div class="forum-card"><div class="forum-card-head"><div><div class="forum-card-title">Create Topic</div><div class="forum-card-sub">Post a new forum thread</div></div></div><div class="forum-form"><input id="forum-topic-title" class="form-input" maxlength="80" placeholder="Topic title"><select id="forum-topic-tag" class="form-input"><option>General</option><option>Idea</option><option>Question</option><option>Bug</option><option>Report</option></select><textarea id="forum-topic-body" class="form-input form-textarea" placeholder="Write the first post for this topic..."></textarea><div class="forum-thread-actions"><button class="btn btn-accent" onclick="App.postForumTopic()">Post Topic</button><button class="btn btn-outline" onclick="App.openChat(${q(ch.id)})">Refresh</button></div></div></div><div class="forum-card"><div class="forum-card-head"><div><div class="forum-card-title">Topics</div><div class="forum-card-sub">${roots.length} threads</div></div></div><div class="forum-list">${roots.length?roots.map(topic=>{const meta=this._forumTopicMeta(topic);const replyCount=this._forumReplies(all,topic.id).length;return `<div class="forum-topic ${String(topic.id)===String(this._forumTopicId)?'active':''}" onclick='App.openForumTopic(${topic.id})'><div class="forum-topic-top"><div class="forum-topic-title">${esc(meta.title)}</div><span class="forum-pill">${replyCount}</span></div><div class="forum-badges"><span class="forum-badge">${esc(meta.tag||'General')}</span>${meta.pinned?'<span class="forum-badge forum-pinned">Pinned</span>':''}${meta.locked?'<span class="forum-badge forum-locked">Locked</span>':''}</div><div class="forum-topic-meta">${esc(topic.user_name||topic.user_id||'user')} • ${esc(new Date(topic.created_at).toLocaleString())}</div><div class="forum-topic-body">${esc(meta.preview)}</div></div>`;}).join(''):`<div class="forum-empty">No topics yet. Create the first one.</div>`}</div></div></div><div class="forum-col"><div class="forum-card"><div class="forum-card-head"><div><div class="forum-card-title">${activeMeta?esc(activeMeta.title):'Open a Topic'}</div><div class="forum-card-sub">${active?`${esc(active.user_name||active.user_id||'user')} • ${esc(new Date(active.created_at).toLocaleString())}`:'Choose a topic from the left side.'}</div></div>${active&&this.isStaff()?`<div class="site-actions"><button class="btn btn-outline" onclick="App.toggleForumPin(${active.id})">${activeMeta?.pinned?'Unpin':'Pin'}</button><button class="btn btn-outline" onclick="App.toggleForumLock(${active.id})">${activeMeta?.locked?'Unlock':'Lock'}</button></div>`:''}</div>${active?`<div class="forum-thread"><div class="forum-post"><div class="forum-post-head"><div class="forum-post-author">${esc(active.user_name||active.user_id||'user')}</div><div class="forum-post-time">${esc(new Date(active.created_at).toLocaleString())}</div></div><div class="forum-badges"><span class="forum-badge">${esc(activeMeta.tag||'General')}</span>${activeMeta.pinned?'<span class="forum-badge forum-pinned">Pinned</span>':''}${activeMeta.locked?'<span class="forum-badge forum-locked">Locked</span>':''}</div><div class="forum-post-body">${esc(activeMeta.body||activeMeta.title)}</div></div><div class="forum-card-sub">${replies.length} replies</div><div class="forum-replies">${replies.length?replies.map(reply=>`<div class="forum-reply"><div class="forum-post-head"><div class="forum-post-author">${esc(reply.user_name||reply.user_id||'user')}</div><div class="forum-post-time">${esc(new Date(reply.created_at).toLocaleString())}</div></div><div class="forum-post-body">${esc(reply.content||'')}</div></div>`).join(''):`<div class="forum-empty">No replies yet. Be the first to answer.</div>`}</div>${replyLocked?`<div class="forum-empty">This topic is locked. Only moderators can reply.</div>`:`<div class="forum-reply-box"><textarea id="forum-reply-body" class="form-input form-textarea" placeholder="Write a reply to this topic..."></textarea><div class="forum-thread-actions"><button class="btn btn-accent" onclick="App.postForumReply(${active.id})">Reply</button></div></div>`}</div>`:`<div class="forum-empty">Pick a topic on the left to read replies.</div>`}</div><div class="forum-card"><div class="forum-card-head"><div><div class="forum-card-title">Quick Uses</div><div class="forum-card-sub">Good places to use the forum</div></div></div><div class="forum-quick"><div class="dc-home-link"><span>Ideas</span><strong>POST</strong></div><div class="dc-home-link"><span>Questions</span><strong>ASK</strong></div><div class="dc-home-link"><span>Reports</span><strong>THREAD</strong></div><div class="dc-home-link"><span>Feedback</span><strong>OPEN</strong></div></div></div></div></div>`;
    this._sub=sb.channel('forum-'+ch.id).on('postgres_changes',{event:'*',schema:'public',table:'chaty_messages',filter:'channel_id=eq.'+ch.id},payload=>{
      if(this.ch!==ch.id)return;
      if(payload?.eventType==='INSERT'&&this._registerLiveTraffic()){this._liveTrafficDropped++;return;}
      this._scheduleForumRefresh(ch,payload?.eventType==='INSERT'?320:180);
    }).subscribe();
  },
  openForumTopic(id){
    this._forumTopicId=id;
    if(this.ch)this.openChat(this.ch);
  },
  async postForumTopic(){
    if(!this._requireDb()||!this.ch)return;
    const title=(document.getElementById('forum-topic-title')?.value||'').trim().slice(0,80);
    const tag=(document.getElementById('forum-topic-tag')?.value||'General').trim().slice(0,18);
    const body=(document.getElementById('forum-topic-body')?.value||'').trim().slice(0,this._maxMessageLength);
    if(!title){alert('Topic title is required.');return;}
    const content=buildForumTopic(title,body,{tag});
    const guard=this._messageGuard(`${title} ${body}`.trim());
    if(!guard.ok){alert(guard.msg);return;}
    const {data,error}=await sb.from('chaty_messages').insert({channel_id:this.ch,user_id:this._session.id,user_name:this._displayName(this._me||{id:this._session.id,display_name:this._session.name},this._session.id),content,platform:'chaty'}).select('id').single();
    if(error){alert(error.message);return;}
    this._forumTopicId=data?.id||null;
    this.openChat(this.ch);
  },
  async postForumReply(topicId){
    if(!this._requireDb()||!this.ch||!topicId)return;
    const {data:topic}=await sb.from('chaty_messages').select('content').eq('id',topicId).single();
    const topicMeta=parseForumTopic(topic?.content||'');
    if(topicMeta.locked&&!this.isStaff()){alert('This topic is locked.');return;}
    const body=(document.getElementById('forum-reply-body')?.value||'').trim().slice(0,this._maxMessageLength);
    if(!body){alert('Reply is empty.');return;}
    const guard=this._messageGuard(body);
    if(!guard.ok){alert(guard.msg);return;}
    const {error}=await sb.from('chaty_messages').insert({channel_id:this.ch,user_id:this._session.id,user_name:this._displayName(this._me||{id:this._session.id,display_name:this._session.name},this._session.id),content:body,platform:'chaty',reply_to:topicId});
    if(error){alert(error.message);return;}
    this._forumTopicId=topicId;
    this.openChat(this.ch);
  },
  async _updateForumTopic(topicId,patch){
    if(!this._requireDb()||!this.isStaff())return;
    const {data:topic}=await sb.from('chaty_messages').select('content').eq('id',topicId).single();
    const meta=parseForumTopic(topic?.content||'');
    const next={...meta,...patch};
    await sb.from('chaty_messages').update({content:buildForumTopic(next.title,next.body,next)}).eq('id',topicId);
  },
  async toggleForumLock(topicId){
    const {data:topic}=await sb.from('chaty_messages').select('content').eq('id',topicId).single();
    const meta=parseForumTopic(topic?.content||'');
    await this._updateForumTopic(topicId,{locked:!meta.locked});
  },
  async toggleForumPin(topicId){
    const {data:topic}=await sb.from('chaty_messages').select('content').eq('id',topicId).single();
    const meta=parseForumTopic(topic?.content||'');
    await this._updateForumTopic(topicId,{pinned:!meta.pinned});
  },
  _ensureToastHost(){
    let host=document.getElementById('dc-toast-stack');
    if(host)return host;
    host=document.createElement('div');
    host.id='dc-toast-stack';
    host.className='dc-toast-stack';
    document.body.appendChild(host);
    return host;
  },
  _showToast(title,body='',meta='',onClick=null){
    const host=this._ensureToastHost();
    const toast=document.createElement('div');
    toast.className='dc-toast';
    toast.innerHTML=`<div class="dc-toast-title">${esc(title)}</div><div class="dc-toast-body">${esc(body)}</div>${meta?`<div class="dc-toast-meta">${esc(meta)}</div>`:''}`;
    toast.onclick=()=>{toast.remove();if(typeof onClick==='function')onClick();};
    host.prepend(toast);
    setTimeout(()=>toast.remove(),5200);
  },
  _scheduleLoadChs(delay=450){
    clearTimeout(this._loadChsTimer);
    this._loadChsTimer=setTimeout(()=>{
      if(this._session)this.loadChs(true);
    },Math.max(120,delay|0));
  },
  _scheduleChatRefresh(delay=300){
    clearTimeout(this._chatRefreshTimer);
    this._chatRefreshTimer=setTimeout(()=>{
      if(this.page==='chat'&&this.ch)this._refreshOpenChat();
    },Math.max(120,delay|0));
  },
  _scheduleForumRefresh(ch,delay=350){
    clearTimeout(this._forumRefreshTimer);
    this._forumRefreshTimer=setTimeout(()=>{
      if(this.page==='chat'&&this.ch===ch?.id)this._openForum(ch);
    },Math.max(150,delay|0));
  },
  _registerLiveTraffic(){
    const now=Date.now();
    this._liveTrafficHits=(this._liveTrafficHits||[]).filter(ts=>now-ts<this._liveTrafficWindowMs);
    this._liveTrafficHits.push(now);
    if(now<this._liveTrafficUntil)return true;
    if(this._liveTrafficHits.length<this._liveTrafficLimit)return false;
    this._liveTrafficUntil=now+this._liveTrafficSuspendMs;
    this._liveTrafficDropped=0;
    clearTimeout(this._liveTrafficTimer);
    this._showToast('Heavy traffic shield','Live updates are paused for a few seconds so the page stays responsive.','Flood protection');
    this._setComposerState(`Heavy traffic detected. Live updates pause for ${Math.ceil(this._liveTrafficSuspendMs/1000)}s to protect the client.`,'warn');
    this._liveTrafficTimer=setTimeout(()=>{
      const dropped=this._liveTrafficDropped||0;
      this._liveTrafficUntil=0;
      this._liveTrafficDropped=0;
      if(this.page==='chat'&&this.ch)this._scheduleChatRefresh(120);
      if(dropped)this._showToast('Live feed recovered',`${dropped} fast updates were collapsed while protection was active.`,'Recovered');
    },this._liveTrafficSuspendMs);
    return true;
  },
  _trafficShieldActive(){
    return Date.now()<this._liveTrafficUntil;
  },
  _trimRenderedMessages(){
    const list=document.getElementById('dc-msg-list');
    if(!list)return;
    let groups=[...list.querySelectorAll('.dc-msg-group')];
    let count=list.querySelectorAll('[data-msg-id]').length;
    while(count>this._maxRenderedMessages&&groups.length){
      const victim=groups.shift();
      if(!victim)break;
      count-=victim.querySelectorAll('[data-msg-id]').length;
      const prev=victim.previousElementSibling;
      victim.remove();
      if(prev?.classList?.contains('dc-date-div')&&!prev.nextElementSibling?.classList?.contains('dc-msg-group'))prev.remove();
    }
  },
  _homeHtml(activeWarnings=[]){
    const users=this._lastUsers||[];
    const channels=this._lastChannels||[];
    const me=this._me||{};
    const standing=this._warningInfo(me);
    const publicChannels=channels.filter(c=>c.type==='public').slice(0,6);
    const favorites=this._favoriteChannels().slice(0,5);
    const recentDms=this._recentDmChannels(5);
    const commandRows=['/help','/roll 20','/8ball question','/choose red | blue','/coin','/poll Lunch? | Pizza | Tacos'];
    const news=this._homeNews||parseHomeNews('');
    const newsTone={info:'READY',good:'LIVE',warn:'NOTICE',hot:'HOT'}[news.tone||'info']||'READY';
    const newsWhen=news.updatedAt?this._relativeTime(new Date(news.updatedAt).getTime()):'now';
    return `<div class="dc-home"><div class="dc-home-hero"><div class="dc-home-kicker">School Server</div><div class="dc-home-title">Welcome to DIHCORD</div><div class="dc-home-text">This update leans harder into convenience: faster inbox scanning, favorites, richer DM previews, quick actions and better little touches across the app.</div></div><div class="dc-home-grid"><div class="dc-home-card"><h3>Current Version</h3><p>${esc(news.body||'Welcome to the latest DIHCORD build.')}</p><div class="dc-home-list"><div class="dc-home-link"><span>${esc(news.title||'DIHCORD Updates')}</span><strong>${esc(news.version||'V20.3')}</strong></div><div class="dc-home-link"><span>Owner news</span><strong>${esc(newsTone)}</strong></div><div class="dc-home-link"><span>Updated</span><strong>${esc(newsWhen)}</strong></div></div></div><div class="dc-home-card"><h3>Community Snapshot</h3><p>${users.length} accounts, ${publicChannels.length||channels.filter(c=>c.type==='public').length} public rooms and active student chats.</p><div class="dc-home-list"><div class="dc-home-link"><span>Active accounts</span><strong>${users.length}</strong></div><div class="dc-home-link"><span>Staff team</span><strong>${users.filter(u=>u.role==='owner'||u.role==='mod').length}</strong></div><div class="dc-home-link"><span>Unread DMs</span><strong>${this._totalUnread()}</strong></div></div></div><div class="dc-home-card"><h3>Your Standing</h3><p>${esc(standing.detail)}</p><div class="dc-home-list"><div class="dc-home-link"><span>Account state</span>${this._warningChip(me)}</div><div class="dc-home-link"><span>Total warnings</span><strong>${standing.count}</strong></div><div class="dc-home-link"><span>Active reasons</span><strong>${activeWarnings.length}</strong></div></div></div><div class="dc-home-card"><h3>Inbox</h3><p>Mentions, forum replies and DM alerts now collect in one spot.</p><div class="dc-home-list"><div class="dc-home-link" onclick="App.goInbox()"><span>Unread inbox</span><strong>${this._inboxUnreadCount()}</strong></div><div class="dc-home-link" onclick="App.goInbox()"><span>Latest alert</span><strong>${esc(this._relativeTime(this._inboxItems?.[0]?.ts)||'none')}</strong></div><div class="dc-home-link" onclick="App.goSettings()"><span>Site settings</span><strong>OPEN</strong></div></div></div><div class="dc-home-card"><h3>Local Tools</h3><p>Keep private helpers on this device without touching the server or database.</p><div class="dc-home-list"><div class="dc-home-link" onclick="App.goSaved()"><span>Saved messages</span><strong>${this._savedCount()}</strong></div><div class="dc-home-link" onclick="App.goSettings()"><span>Drafts</span><strong>${this._draftCount()}</strong></div><div class="dc-home-link" onclick="App.goSettings()"><span>Muted rooms</span><strong>${Object.keys(this._mutedChannels||{}).length}</strong></div></div></div><div class="dc-home-card"><h3>Favorites</h3><p>Pin your most-used rooms so they stay easy to reach.</p><div class="dc-home-list">${favorites.length?favorites.map(c=>`<div class="dc-home-link" onclick='App.openChat(${q(c.id)})'><span>${esc(c.name.replace(/^#\s*/,''))}</span><strong>${esc(this._channelGlyph(c))}</strong></div>`).join(''):'<div class="dc-home-link"><span>No favorites yet</span><strong>STAR</strong></div>'}</div></div><div class="dc-home-card"><h3>Recent DMs</h3><p>Your freshest direct chats stay visible here.</p><div class="dc-home-list">${recentDms.length?recentDms.map(c=>{const otherId=(c.members||[]).find(m=>m!==this._session?.id);const user=this._cache[otherId];const label=this._displayName(user||{id:otherId,display_name:otherId},otherId);const meta=this._dmMeta[c.id]||{};const unread=this._unreadCount(c.id);return `<div class="dc-home-link" onclick='App.openChat(${q(c.id)})'><span>${esc(label)}${unread?` (${unread})`:''}</span><strong>${esc(this._relativeTime(meta.ts)||'DM')}</strong></div>`;}).join(''):'<div class="dc-home-link"><span>No DM activity yet</span><strong>-</strong></div>'}</div></div><div class="dc-home-card"><h3>Command Deck</h3><p>Quick fun and utility commands you can fire right in chat.</p><div class="dc-home-list">${commandRows.map(cmd=>`<div class="dc-home-link"><span>${esc(cmd)}</span><strong>READY</strong></div>`).join('')}</div></div><div class="dc-home-card"><h3>Popular Channels</h3><p>Jump into the busiest public rooms from here.</p><div class="dc-home-list">${publicChannels.map(c=>`<div class="dc-home-link" onclick='App.openChat(${q(c.id)})'><span>${esc(c.name.replace(/^#\s*/,''))}</span><strong>#</strong></div>`).join('')||'<div class="dc-home-link"><span>No public channels yet</span><strong>-</strong></div>'}</div></div></div></div>`;
  },
  _bindWindowState(){
    if(this._visibilityHooked)return;
    this._visibilityHooked=true;
    document.addEventListener('visibilitychange',()=>{
      if(document.visibilityState==='visible'&&this.page==='chat'&&this.ch){
        const channel=(this._lastChannels||[]).find(c=>c.id===this.ch);
        if(channel?.type==='dm')this._markRead(this.ch);
      }else this._updateTitle();
    });
    window.addEventListener('focus',()=>{
      if(this.page==='chat'&&this.ch){
        const channel=(this._lastChannels||[]).find(c=>c.id===this.ch);
        if(channel?.type==='dm')this._markRead(this.ch);
      }
    });
  },
  _requestNotifyPermission(){
    if(!this._settings.desktopNotices||!('Notification'in window))return;
    if(Notification.permission==='default')Notification.requestPermission().catch(()=>{});
  },
  _setupInboxSub(){
    if(!sbReady()||!this._session?.id)return;
    if(this._inboxSub)sb.removeChannel(this._inboxSub);
    this._inboxSub=sb.channel('inbox-'+this._session.id).on('postgres_changes',{event:'INSERT',schema:'public',table:'chaty_messages'},payload=>this._handleInboxMessage(payload.new)).subscribe();
  },
  async _handleInboxMessage(msg){
    if(!msg||msg.user_id===this._session?.id||this._trafficShieldActive())return;
    let channel=(this._lastChannels||[]).find(c=>c.id===msg.channel_id);
    if(!channel)return;
    const localMuted=this._isChannelMuted(channel.id);
    const rawContent=String(msg.content||'');
    if(channel.type!=='dm'&&channel.id!=='announcements'&&!(channel.type==='forum'&&msg.reply_to)&&!rawContent.includes('@'))return;
    const incomingText=this._messagePreview(msg,72);
    const from=this._displayName(this._cache[msg.user_id]||{id:msg.user_id,display_name:msg.user_name},msg.user_name||msg.user_id);
    if(channel.id==='announcements'){
      this._addInboxItem({type:'announcement',title:'New announcement',body:incomingText,channelId:channel.id});
      if(localMuted)return;
      this._showToast('New announcement',incomingText,'Open channel',()=>this.openChat(channel.id));
      return;
    }
    if(channel.type==='dm'&&(channel.members||[]).includes(this._session.id)){
      const viewingSameDm=this.page==='chat'&&this.ch===channel.id;
      if(viewingSameDm&&document.visibilityState==='visible'){this._markRead(channel.id);return;}
      this._bumpUnread(channel.id);
      this._addInboxItem({type:'dm',title:from,body:incomingText,channelId:channel.id});
      this._dmMeta[channel.id]={ts:new Date(msg.created_at||Date.now()).getTime(),content:msg.content||'',user_id:msg.user_id||'',user_name:msg.user_name||''};
      this._scheduleLoadChs(700);
      if(localMuted)return;
      if(!viewingSameDm)this._snd();
      this._showToast(from,incomingText,'Direct message',()=>this.openChat(channel.id));
      if(document.hidden&&this._settings.desktopNotices&&'Notification'in window&&Notification.permission==='granted'){
        const note=new Notification(from,{body:String(this._messagePlainText(msg)||'New message').slice(0,140),tag:'dm-'+channel.id});
        note.onclick=()=>{window.focus();this.openChat(channel.id);note.close();};
        setTimeout(()=>note.close(),5000);
      }
      return;
    }
    if(this._mentionsCurrentUser(this._messagePlainText(msg))){
      this._addInboxItem({type:'mention',title:`Mention from ${from}`,body:incomingText,channelId:channel.id,topicId:channel.type==='forum'?(msg.reply_to||msg.id):null});
      this._showToast(`Mention from ${from}`,incomingText,'Open message',()=>{if(channel.type==='forum')this._forumTopicId=msg.reply_to||msg.id;this.openChat(channel.id);});
      if(document.hidden&&this._settings.desktopNotices&&'Notification'in window&&Notification.permission==='granted'){
        const note=new Notification(`Mention from ${from}`,{body:incomingText,tag:'mention-'+channel.id});
        note.onclick=()=>{window.focus();if(channel.type==='forum')this._forumTopicId=msg.reply_to||msg.id;this.openChat(channel.id);note.close();};
        setTimeout(()=>note.close(),5000);
      }
      this._snd();
      return;
    }
    if(channel.type==='forum'&&msg.reply_to){
      const {data:parent}=await sb.from('chaty_messages').select('id,user_id,reply_to').eq('id',msg.reply_to).single();
      const topicId=parent?.reply_to||parent?.id||msg.reply_to;
      if(parent?.user_id===this._session?.id){
        this._addInboxItem({type:'forum',title:`Forum reply from ${from}`,body:incomingText,channelId:channel.id,topicId});
        if(localMuted)return;
        this._showToast(`Forum reply from ${from}`,incomingText,'Open topic',()=>{this._forumTopicId=topicId;this.openChat(channel.id);});
        this._snd();
      }
    }
  },
  _hydrateUiPrefs(){
    this._hydrateSettings();
    this._theme=localStorage.getItem(this._themeKey)||'dark';
    this._navExpanded=localStorage.getItem(this._navKey)==='1';
    this._hydrateFavorites();
    this._hydrateDrafts();
    this._hydrateSavedMessages();
    this._hydrateMutedChannels();
    this._applyTheme(this._theme);
    this._syncNavShell();
  },
  _applyTheme(theme='dark'){
    this._theme=theme==='light'?'light':'dark';
    document.body.classList.toggle('light-theme',this._theme==='light');
    document.body.classList.toggle('dark-theme',this._theme==='dark');
    localStorage.setItem(this._themeKey,this._theme);
  },
  toggleTheme(){
    this._applyTheme(this._theme==='light'?'dark':'light');
    if(this._me)this._renderUserPanel(this._me);
  },
  _syncNavShell(){
    const shell=document.getElementById('dc-nav-shell');
    const label=document.getElementById('dc-nav-toggle-label');
    if(!shell)return;
    shell.classList.toggle('expanded',!!this._navExpanded);
    shell.classList.toggle('collapsed',!this._navExpanded);
    if(label)label.textContent=this._navExpanded?'Hide Menu':'Open Menu';
  },
  toggleQuickNav(){
    this._navExpanded=!this._navExpanded;
    localStorage.setItem(this._navKey,this._navExpanded?'1':'0');
    this._syncNavShell();
  },
  goInbox(){
    this.page='inbox';this.ch=null;this.replyTo=null;this._closeLiveSubs();
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
    document.getElementById('nav-inbox')?.classList.add('dc-active');
    document.getElementById('dc-members')?.classList.add('hidden');
    const items=this._inboxItems||[];
    const rows=items.length?items.map((item,idx)=>{
      return '<div class="inbox-item '+(item.read?'':'unread')+'" data-inbox-index="'+idx+'">'+
        '<div class="inbox-top"><div class="inbox-title">'+esc(item.title||'Update')+'</div>'+
        '<div class="inbox-meta">'+esc(this._relativeTime(item.ts)||'now')+'</div></div>'+
        '<div class="inbox-body">'+esc(item.body||'')+'</div></div>';
    }).join(''):'<div class="forum-empty">Your inbox is empty right now.</div>';
    const area=document.getElementById('chat-area');
    area.innerHTML='<div class="site-shell"><div class="site-hero"><div class="site-title">Inbox</div>'+
      '<div class="site-sub">Mentions, DM alerts, forum replies and server updates land here so nothing important gets lost.</div></div>'+
      '<div class="site-grid"><div class="site-card"><div class="site-card-head"><div>'+
      '<div class="site-card-title">Notifications</div><div class="site-card-sub">'+items.length+' total • '+this._inboxUnreadCount()+' unread</div></div>'+
      '<div class="site-actions"><button class="btn btn-outline" id="inbox-mark-read">Mark all read</button></div></div>'+
      '<div class="site-list">'+rows+'</div></div></div></div>';
    document.getElementById('inbox-mark-read')?.addEventListener('click',()=>{this._markAllInboxRead();this.goInbox();});
    area.querySelectorAll('[data-inbox-index]').forEach(el=>{
      el.addEventListener('click',()=>{const item=items[Number(el.dataset.inboxIndex)];if(item)this.openInboxItem(item.id);});
    });
  },
  goSaved(){
    this.page='saved';this.ch=null;this.replyTo=null;this._closeLiveSubs();
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
    document.getElementById('nav-saved')?.classList.add('dc-active');
    document.getElementById('dc-members')?.classList.add('hidden');
    const items=[...(this._savedMessages||[])].sort((a,b)=>(b.savedAt||0)-(a.savedAt||0));
    const rows=items.length?items.map((item,idx)=>{
      return '<div class="inbox-item" data-saved-index="'+idx+'">'+
        '<div class="inbox-top"><div class="inbox-title">'+esc(this._channelLabel(item.channelId))+'</div>'+
        '<div class="inbox-meta">'+esc(this._relativeTime(item.savedAt)||'now')+'</div></div>'+
        '<div class="inbox-body"><strong>'+esc(item.author||'user')+'</strong> • '+esc(item.preview||'Saved message')+'</div>'+
        '<div class="site-actions" style="margin-top:10px">'+
        '<button class="btn btn-outline" data-saved-open="'+idx+'">Open</button>'+
        '<button class="btn btn-outline" data-saved-remove="'+idx+'">Remove</button>'+
        '</div></div>';
    }).join(''):'<div class="forum-empty">You have no saved messages yet. Use the SV button on a message to keep it here.</div>';
    const area=document.getElementById('chat-area');
    area.innerHTML='<div class="site-shell"><div class="site-hero"><div class="site-title">Saved Messages</div>'+
      '<div class="site-sub">Keep useful posts on this device. These bookmarks are private and do not add load to the server.</div></div>'+
      '<div class="site-grid"><div class="site-card"><div class="site-card-head"><div>'+
      '<div class="site-card-title">Local Bookmarks</div><div class="site-card-sub">'+items.length+' saved</div></div>'+
      '<div class="site-actions"><button class="btn btn-outline" id="saved-clear">Clear all</button></div></div>'+
      '<div class="site-list">'+rows+'</div></div></div></div>';
    document.getElementById('saved-clear')?.addEventListener('click',()=>this._clearSavedMessages());
    area.querySelectorAll('[data-saved-index]').forEach(el=>{
      el.addEventListener('click',()=>{const item=items[Number(el.dataset.savedIndex)];if(item)this.openSavedItem(item.id);});
    });
    area.querySelectorAll('[data-saved-open]').forEach(btn=>{
      btn.addEventListener('click',event=>{event.stopPropagation();const item=items[Number(btn.dataset.savedOpen)];if(item)this.openSavedItem(item.id);});
    });
    area.querySelectorAll('[data-saved-remove]').forEach(btn=>{
      btn.addEventListener('click',event=>{event.stopPropagation();const item=items[Number(btn.dataset.savedRemove)];if(item)this._removeSavedMessage(item.id);});
    });
  },
  openInboxItem(id){
    const item=(this._inboxItems||[]).find(entry=>entry.id===id);
    if(!item)return;
    this._markInboxItemRead(id);
    if(item.channelId){
      if(item.topicId)this._forumTopicId=item.topicId;
      this.openChat(item.channelId);
      return;
    }
    this.goInbox();
  },
  goSettings(){
    this.page='settings';this.ch=null;this.replyTo=null;this._closeLiveSubs();
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
    document.getElementById('nav-settings')?.classList.add('dc-active');
    document.getElementById('dc-members')?.classList.add('hidden');
    const mutedIds=Object.keys(this._mutedChannels||{});
    document.getElementById('chat-area').innerHTML=`<div class="site-shell"><div class="site-hero"><div class="site-title">Site Settings</div><div class="site-sub">Tune how DIHCORD looks and feels on your device without touching the server for everyone else.</div></div><div class="site-grid"><div class="site-card"><div class="site-card-head"><div><div class="site-card-title">Appearance</div><div class="site-card-sub">Theme and layout</div></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Theme</div><div class="site-row-sub">Choose between dark and light mode.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.updateSetting('theme',this.value)"><option value="dark" ${this._theme==='dark'?'selected':''}>Dark</option><option value="light" ${this._theme==='light'?'selected':''}>Light</option></select></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Quick menu default</div><div class="site-row-sub">Keep the Home/Profile/Inbox menu open by default.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.updateSetting('menuOpen',this.value)"><option value="0" ${!this._navExpanded?'selected':''}>Closed</option><option value="1" ${this._navExpanded?'selected':''}>Open</option></select></div></div></div><div class="site-card"><div class="site-card-head"><div><div class="site-card-title">Notifications</div><div class="site-card-sub">Alerts and sound</div></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Desktop notifications</div><div class="site-row-sub">Allow browser popups for DMs, mentions and forum replies.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.updateSetting('desktopNotices',this.value)"><option value="1" ${this._settings.desktopNotices!==false?'selected':''}>On</option><option value="0" ${this._settings.desktopNotices===false?'selected':''}>Off</option></select></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Message sounds</div><div class="site-row-sub">Play a sound for incoming DMs and alerts.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.updateSetting('sounds',this.value)"><option value="1" ${this._settings.sounds!==false?'selected':''}>On</option><option value="0" ${this._settings.sounds===false?'selected':''}>Off</option></select></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">DM previews</div><div class="site-row-sub">Show the last message text inside the DM list.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.updateSetting('dmPreviews',this.value)"><option value="1" ${this._settings.dmPreviews!==false?'selected':''}>On</option><option value="0" ${this._settings.dmPreviews===false?'selected':''}>Off</option></select></div></div></div><div class="site-card"><div class="site-card-head"><div><div class="site-card-title">Chat Tools</div><div class="site-card-sub">Local-only upgrades for your device</div></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Saved messages</div><div class="site-row-sub">Bookmarks that stay only on this computer.</div></div><div class="site-actions"><button class="btn btn-outline" onclick="App.goSaved()">Open (${this._savedCount()})</button><button class="btn btn-outline" onclick="App._clearSavedMessages()">Clear</button></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Drafts</div><div class="site-row-sub">One draft per channel or DM, restored automatically.</div></div><div class="site-actions"><button class="btn btn-outline" onclick="App.clearAllDrafts()">Clear (${this._draftCount()})</button></div></div>${mutedIds.length?mutedIds.map(id=>`<div class="site-row"><div class="site-row-copy"><div class="site-row-title">${esc(this._channelLabel(id))}</div><div class="site-row-sub">Local mute is active. This room stays silent on this device.</div></div><div class="site-actions"><button class="btn btn-outline" onclick='App.toggleChannelMute(${q(id)})'>Unmute</button><button class="btn btn-outline" onclick='App.openChat(${q(id)})'>Open</button></div></div>`).join(''):`<div class="site-row"><div class="site-row-copy"><div class="site-row-title">Muted rooms</div><div class="site-row-sub">No local mutes are active right now.</div></div><div class="site-actions"><strong>0</strong></div></div>`}</div></div></div>`;
  },
  updateSetting(key,value){
    if(key==='theme'){this._applyTheme(value);if(this._me)this._renderUserPanel(this._me);this.goSettings();return;}
    if(key==='menuOpen'){this._navExpanded=value==='1';localStorage.setItem(this._navKey,this._navExpanded?'1':'0');this._syncNavShell();this.goSettings();return;}
    this._settings[key]=value==='1';
    this._persistSettings();
    if(key==='desktopNotices'&&this._settings.desktopNotices)this._requestNotifyPermission();
    if(key==='dmPreviews')this.loadChs();
    this.goSettings();
  },
  _mentionsCurrentUser(text){
    return mentionCandidates(this._me||this._session).some(name=>new RegExp(`(^|\\s)@${name}(?=\\b|\\s|$)`,'i').test(String(text||'')));
  },
  _messagePlainText(msg){
    const image=parseImageContent(msg?.content||'');
    if(image)return image.caption?`Image: ${image.caption}`:`Image: ${image.name||'upload'}`;
    const poll=parsePollContent(msg?.content||'');
    if(poll)return `${poll.question} ${poll.options.join(' ')}`.trim();
    if((this._lastChannels||[]).find(c=>c.id===msg?.channel_id)?.type==='forum'&&!msg?.reply_to){
      const topic=parseForumTopic(msg?.content||'');
      return `${topic.title} ${topic.body}`.trim();
    }
    return String(msg?.content||'');
  },
  _messagePreview(msg,max=72){
    return this._textSnippet(this._messagePlainText(msg),max);
  },
  _rawContentPreview(raw,max=72){
    const image=parseImageContent(raw);
    if(image)return this._textSnippet(image.caption?`Image: ${image.caption}`:`Image: ${image.name||'upload'}`,max);
    const poll=parsePollContent(raw);
    if(poll)return this._textSnippet(`Poll: ${poll.question}`,max);
    return this._textSnippet(raw,max);
  },
  _estimateDataUrlBytes(dataUrl=''){
    const base64=(String(dataUrl).split(',')[1]||'');
    const pad=((base64.match(/=*$/)||[''])[0]||'').length;
    return Math.max(0,Math.floor(base64.length*3/4)-pad);
  },
  _formatBytes(bytes=0){
    const n=Math.max(0,Number(bytes)||0);
    if(n>=1024*1024)return `${(n/(1024*1024)).toFixed(1)} MB`;
    if(n>=1024)return `${Math.round(n/1024)} KB`;
    return `${n} B`;
  },
  _safeUploadName(name='image'){
    const dot=name.lastIndexOf('.');
    const base=(dot>0?name.slice(0,dot):name).toLowerCase().replace(/[^a-z0-9_-]+/g,'-').replace(/^-+|-+$/g,'').slice(0,48)||'image';
    const ext=(dot>0?name.slice(dot+1):'').toLowerCase().replace(/[^a-z0-9]/g,'').slice(0,8);
    return ext?`${base}.${ext}`:base;
  },
  async _fileToDataUrl(file){
    return await new Promise((resolve,reject)=>{
      const reader=new FileReader();
      reader.onload=()=>resolve(String(reader.result||''));
      reader.onerror=()=>reject(new Error('Failed to read file.'));
      reader.readAsDataURL(file);
    });
  },
  async _loadImageElement(file){
    const objectUrl=URL.createObjectURL(file);
    try{
      return await new Promise((resolve,reject)=>{
        const img=new Image();
        img.onload=()=>resolve(img);
        img.onerror=()=>reject(new Error('Failed to load image.'));
        img.src=objectUrl;
      });
    }finally{
      URL.revokeObjectURL(objectUrl);
    }
  },
  async _compressStaticImage(file){
    const img=await this._loadImageElement(file);
    const maxSide=1280;
    const ratio=Math.min(1,maxSide/Math.max(img.width||1,img.height||1));
    const width=Math.max(1,Math.round((img.width||1)*ratio));
    const height=Math.max(1,Math.round((img.height||1)*ratio));
    const canvas=document.createElement('canvas');
    canvas.width=width;
    canvas.height=height;
    const ctx=canvas.getContext('2d');
    if(!ctx)throw new Error('Canvas is unavailable for image compression.');
    ctx.drawImage(img,0,0,width,height);
    const blob=await new Promise(resolve=>canvas.toBlob(resolve,'image/webp',0.8));
    if(!blob)throw new Error('Failed to compress image.');
    const base=this._safeUploadName(file.name).replace(/\.[a-z0-9]+$/i,'');
    return new File([blob],`${base}.webp`,{type:blob.type||'image/webp'});
  },
  async _prepareUploadPayload(file){
    const kind=String(file?.type||'').toLowerCase();
    if(!/^image\/(png|jpe?g|webp|gif)$/i.test(kind))throw new Error('Use PNG, JPG, WEBP or GIF.');
    if(kind==='image/gif'&&(file?.size||0)>this._maxGifUploadBytes)throw new Error(`GIF is too large. Max ${this._formatBytes(this._maxGifUploadBytes)}.`);
    if((file?.size||0)>this._maxUploadBytes)throw new Error(`Image is too large. Max ${this._formatBytes(this._maxUploadBytes)}.`);
    let uploadFile=file;
    if(kind!=='image/gif')uploadFile=await this._compressStaticImage(file);
    return{name:file.name||'image',mime:uploadFile.type||kind,size:uploadFile.size||file.size||0,file:uploadFile,dataUrl:await this._fileToDataUrl(uploadFile)};
  },
  _renderPendingUpload(){
    const box=document.getElementById('dc-upload-preview');
    if(!box)return;
    const item=this._pendingUpload;
    if(!item){
      box.classList.add('hidden');
      box.innerHTML='';
      return;
    }
    box.classList.remove('hidden');
    box.innerHTML=`<img class="dc-upload-thumb" src="${attr(item.dataUrl)}" alt="upload preview"><div class="dc-upload-copy"><div class="dc-upload-name">${esc(item.name||'image')}</div><div class="dc-upload-sub">${esc(this._formatBytes(item.size))} • ready to send</div></div><button class="dc-upload-clear" onclick="App.clearPendingUpload()" title="Remove image">✕</button>`;
  },
  clearPendingUpload(){
    this._pendingUpload=null;
    const picker=document.getElementById('chat-file');
    if(picker)picker.value='';
    this._renderPendingUpload();
  },
  pickImage(){
    document.getElementById('chat-file')?.click();
  },
  async handleImagePick(input){
    const file=input?.files?.[0];
    if(!file)return;
    try{
      this._setComposerState('Preparing image...');
      this._pendingUpload=await this._prepareUploadPayload(file);
      this._renderPendingUpload();
      this._setComposerState('Image ready. Add a caption or press Enter to send.');
    }catch(err){
      this._pendingUpload=null;
      this._renderPendingUpload();
      this._setComposerState(err?.message||'Image upload failed.','error');
    }finally{
      if(input)input.value='';
    }
  },
  async _uploadImageAsset(pending){
    if(sb?.storage?.from&&pending?.file){
      try{
        const path=`${this._session?.id||'user'}/${Date.now()}_${this._safeUploadName(pending.name||pending.file.name||'image')}`;
        const {error}=await sb.storage.from(this._uploadBucket).upload(path,pending.file,{upsert:false,contentType:pending.mime||pending.file.type||'image/webp'});
        if(!error){
          const {data}=sb.storage.from(this._uploadBucket).getPublicUrl(path);
          if(data?.publicUrl)return{ok:true,src:data.publicUrl,mode:'storage'};
        }
      }catch{}
    }
    return{
      ok:false,
      error:'Image upload needs the Supabase Storage bucket "chaty-media". The safe fallback stays disabled to protect the database.'
    };
  },
  async _uploadProfileAvatarAsset(file){
    if(!file)return{ok:true,src:''};
    if(String(file.type||'').toLowerCase()==='image/gif')return{ok:false,error:'Profile avatar photos can use PNG, JPG or WEBP. GIF avatars are disabled to save resources.'};
    let pending;
    try{pending=await this._prepareUploadPayload(file);}
    catch(err){return{ok:false,error:err?.message||'Avatar photo failed to prepare.'};}
    if(sb?.storage?.from&&pending?.file){
      try{
        const path=`avatars/${this._session?.id||'user'}/${Date.now()}_${this._safeUploadName(pending.name||pending.file.name||'avatar')}`;
        const {error}=await sb.storage.from(this._uploadBucket).upload(path,pending.file,{upsert:false,contentType:pending.mime||pending.file.type||'image/webp'});
        if(!error){
          const {data}=sb.storage.from(this._uploadBucket).getPublicUrl(path);
          if(data?.publicUrl)return{ok:true,src:data.publicUrl};
        }
      }catch{}
    }
    return{ok:false,error:'Avatar photo upload needs the Supabase Storage bucket "chaty-media". No database fallback is used.'};
  },
  _pollVotes(msg,poll){
    const reactions=msg?.reactions||{};
    return poll.options.map((_,index)=>Array.isArray(reactions[`poll:${index}`])?reactions[`poll:${index}`].length:0);
  },
  _renderPoll(msg,myId){
    const poll=parsePollContent(msg?.content||'');
    if(!poll)return '';
    const votes=this._pollVotes(msg,poll);
    const total=votes.reduce((sum,val)=>sum+val,0);
    const mine=votes.findIndex((_,index)=>Array.isArray(msg?.reactions?.[`poll:${index}`])&&msg.reactions[`poll:${index}`].includes(myId));
    const staffControls=this.isStaff()?`<button class="btn btn-outline" onclick="App.togglePollClosed(${msg.id})" style="margin-top:8px">${poll.closed?'Reopen poll':'Close poll'}</button>`:'';
    return `<div class="poll-shell"><div class="poll-title">${esc(poll.question)}</div><div class="poll-options">${poll.options.map((option,index)=>{const count=votes[index]||0;const pct=total?Math.round((count/total)*100):0;return `<button class="poll-option ${mine===index?'poll-voted':''}" ${poll.closed?'disabled':''} onclick="App.votePoll(${msg.id},${index})"><div class="poll-option-top"><span>${esc(option)}</span><strong>${count}</strong></div><div class="poll-bar"><div class="poll-bar-fill" style="width:${pct}%"></div></div></button>`;}).join('')}</div><div class="poll-meta">${total} vote${total===1?'':'s'}${poll.closed?' / closed':''}</div>${staffControls}</div>`;
  },
  _renderImageMessage(msg){
    const image=parseImageContent(msg?.content||'');
    if(!image)return '';
    return `<div class="poll-shell"><a href="${attr(image.src)}" target="_blank" rel="noopener noreferrer"><img class="dc-gif" src="${attr(image.src)}" loading="lazy" alt="${attr(image.name||'image')}"></a>${image.caption?`<div class="dc-msg-text">${rc(image.caption)}</div>`:''}<div class="poll-meta">${esc(image.name||'image')}</div></div>`;
  },
  async votePoll(id,index){
    if(!this._requireDb())return;
    const {data:msg}=await sb.from('chaty_messages').select('reactions,content').eq('id',id).single();
    const poll=parsePollContent(msg?.content||'');
    if(!poll)return;
    if(poll.closed){alert('This poll is closed.');return;}
    const reactions={...(msg?.reactions||{})};
    poll.options.forEach((_,i)=>{
      const key=`poll:${i}`;
      const list=Array.isArray(reactions[key])?reactions[key].filter(uid=>uid!==this._session.id):[];
      if(list.length)reactions[key]=list;else delete reactions[key];
    });
    const chosen=`poll:${index}`;
    const next=Array.isArray(reactions[chosen])?[...reactions[chosen]]:[];
    next.push(this._session.id);
    reactions[chosen]=next;
    await sb.from('chaty_messages').update({reactions}).eq('id',id);
  },
  async togglePollClosed(id){
    if(!this._requireDb()||!this.isStaff())return;
    const {data:msg}=await sb.from('chaty_messages').select('content').eq('id',id).single();
    const poll=parsePollContent(msg?.content||'');
    if(!poll)return;
    await sb.from('chaty_messages').update({content:buildPollContent(poll.question,poll.options,{closed:!poll.closed})}).eq('id',id);
  },
  async showSearchPanel(){
    const existing=document.getElementById('dc-search-panel');
    if(existing){existing.remove();return;}
    const panel=document.createElement('div');
    panel.id='dc-search-panel';
    panel.className='search-panel';
    panel.innerHTML=`<div class="search-head"><strong>Message Search</strong><button class="dc-act-btn" onclick="document.getElementById('dc-search-panel')?.remove()">✕</button></div><div class="search-body"><div class="search-form"><input id="dc-search-query" class="form-input" placeholder="Search messages..."><select id="dc-search-scope" class="form-input"><option value="current">Current</option><option value="all">All channels</option></select></div><button class="btn btn-accent" onclick="App.runSearch()">Search</button><div id="dc-search-results" class="site-list"><div class="forum-empty">Type something to search.</div></div></div>`;
    document.getElementById('chat-area').appendChild(panel);
    document.getElementById('dc-search-query')?.focus();
  },
  async runSearch(){
    const query=(document.getElementById('dc-search-query')?.value||'').trim().toLowerCase();
    const scope=document.getElementById('dc-search-scope')?.value||'current';
    const box=document.getElementById('dc-search-results');
    if(!box)return;
    if(!query){box.innerHTML='<div class="forum-empty">Enter a search query first.</div>';return;}
    const channelIds=scope==='current'&&this.ch?[this.ch]:(this._lastChannels||[]).filter(c=>c.type!=='dm'||(c.members||[]).includes(this._session?.id)).map(c=>c.id);
    if(query.length<2){box.innerHTML='<div class="forum-empty">Use at least 2 letters for search.</div>';return;}
    const {data:rows,error}=await sb.from('chaty_messages').select('id,channel_id,user_id,user_name,content,platform,reply_to,reactions,pinned,edited,created_at').in('channel_id',channelIds.slice(0,60)).order('created_at',{ascending:false}).limit(120);
    if(error){box.innerHTML=`<div class="forum-empty">${esc(error.message)}</div>`;return;}
    const hits=(rows||[]).filter(msg=>this._messagePlainText(msg).toLowerCase().includes(query)).slice(0,40);
    box.innerHTML=hits.length?hits.map(msg=>{const channel=(this._lastChannels||[]).find(c=>c.id===msg.channel_id);const label=channel?.type==='dm'?'DM':(channel?.name||msg.channel_id);const topicId=channel?.type==='forum'?(msg.reply_to||msg.id):'';return `<div class="search-result" onclick='App.openSearchResult(${q(msg.channel_id)},${q(String(topicId||''))})'><div class="search-result-title">${esc(label.replace(/^#\s*/,''))}</div><div class="search-result-meta">${esc(msg.user_name||msg.user_id||'user')} • ${esc(new Date(msg.created_at).toLocaleString())}</div><div class="search-result-body">${esc(this._messagePreview(msg,140))}</div></div>`;}).join(''):'<div class="forum-empty">No matches found.</div>';
  },
  openSearchResult(channelId,topicId=''){
    document.getElementById('dc-search-panel')?.remove();
    if(topicId)this._forumTopicId=topicId;
    this.openChat(channelId);
  },
  _displayName(user,fallback='user'){return userDisplayName(user,fallback);},
  _avatarGlyph(user,fallback='?'){return userAvatarGlyph(user,fallback);},
  _avatarDecor(user){return userAvatarDecor(user);},
  _avatarImage(user){return userAvatarImage(user);},
  _avatarFrame(user){return userAvatarFrame(user);},
  _profileTheme(user){return userProfileTheme(user);},
  _statusNote(user){return userStatusNote(user);},
  _avatarShell(glyph,color,className,decor='none',extraStyle='',imageUrl='',frame='none'){
    const safeDecor=cleanAvatarDecor(decor);
    const safeFrame=cleanAvatarFrame(frame);
    const decorClass=safeDecor==='none'?'':` av-${safeDecor}`;
    const frameClass=safeFrame==='none'?'':` av-frame-${safeFrame}`;
    const styleSuffix=extraStyle?`;${extraStyle}`:'';
    const photo=txt(imageUrl,'');
    const style=photo?`background:${color} url('${attr(photo)}') center/cover no-repeat${styleSuffix}`:`background:${color}${styleSuffix}`;
    return `<span class="av-shell${decorClass}${frameClass}"><span class="${className} av-core${photo?' av-photo':''}" style="${style}">${photo?'':esc(glyph)}</span></span>`;
  },
  _avatarHtml(user,color,className,fallback='?',extraStyle=''){
    return this._avatarShell(this._avatarGlyph(user,fallback),color,className,this._avatarDecor(user),extraStyle,this._avatarImage(user),this._avatarFrame(user));
  },
  _avatarDecorOptions(){
    return[
      {value:'none',label:'None'},
      {value:'sparkles',label:'Sparkles'},
      {value:'crown',label:'Crown'},
      {value:'orbit',label:'Orbit Ring'},
      {value:'ribbon',label:'Ribbon'},
      {value:'laurel',label:'Laurel'},
      {value:'pixel',label:'Pixel Frame'},
      {value:'confetti',label:'Confetti'},
      {value:'halo',label:'Halo'},
      {value:'bolts',label:'Bolts'},
      {value:'moon',label:'Moon'}
    ];
  },
  _avatarDecorLabel(value){
    return this._avatarDecorOptions().find(item=>item.value===cleanAvatarDecor(value))?.label||'None';
  },
  _avatarFrameOptions(){
    return[
      {value:'none',label:'None'},
      {value:'neon',label:'Neon Glow'},
      {value:'gold',label:'Gold Ring'},
      {value:'ruby',label:'Ruby Pulse'},
      {value:'emerald',label:'Emerald'},
      {value:'frost',label:'Frost'},
      {value:'glitch',label:'Glitch'}
    ];
  },
  _avatarFrameLabel(value){
    return this._avatarFrameOptions().find(item=>item.value===cleanAvatarFrame(value))?.label||'None';
  },
  _profileThemeOptions(){
    return[
      {value:'default',label:'Default'},
      {value:'neon',label:'Neon'},
      {value:'gold',label:'Gold'},
      {value:'candy',label:'Candy'},
      {value:'forest',label:'Forest'},
      {value:'midnight',label:'Midnight'}
    ];
  },
  _profileThemeLabel(value){
    return this._profileThemeOptions().find(item=>item.value===cleanProfileTheme(value))?.label||'Default';
  },
  _updateDecorPreview(){
    const mount=document.getElementById('ep-avatar-preview');
    if(!mount)return;
    const color=document.getElementById('ep-bc')?.value||this._me?.avatar_color||'#5e8ed6';
    const glyph=(document.getElementById('ep-avatar')?.value.trim()||'').slice(0,4)||initial(document.getElementById('ep-dn')?.value||this._session?.id||'U');
    const decor=cleanAvatarDecor(document.getElementById('ep-decor')?.value||'none');
    const frame=cleanAvatarFrame(document.getElementById('ep-frame')?.value||'none');
    const img=document.getElementById('ep-avatar-img-preview')?.value||document.getElementById('ep-avatar-img')?.value||'';
    mount.innerHTML=`${this._avatarShell(glyph,color,'pf-avatar',decor,'',img,frame)}<div class="pf-avatar-preview-copy"><div class="pf-avatar-preview-title">Avatar Preview</div><div class="pf-avatar-preview-sub">${esc(this._avatarDecorLabel(decor))} / ${esc(this._avatarFrameLabel(frame))}</div></div>`;
  },
  async handleProfileAvatarPick(input){
    const file=input?.files?.[0];
    if(!file)return;
    const msg=document.getElementById('ep-upload-msg');
    if(String(file.type||'').toLowerCase()==='image/gif'){
      if(msg)msg.textContent='GIF avatars are disabled to save resources. Use PNG, JPG or WEBP.';
      input.value='';
      return;
    }
    if((file.size||0)>this._maxUploadBytes){
      if(msg)msg.textContent=`Avatar photo is too large. Max ${this._formatBytes(this._maxUploadBytes)}.`;
      input.value='';
      return;
    }
    try{
      if(msg)msg.textContent='Preview ready. The photo uploads when you press Save.';
      const dataUrl=await this._fileToDataUrl(file);
      const preview=document.getElementById('ep-avatar-img-preview');
      if(preview)preview.value=dataUrl;
      this._updateDecorPreview();
    }catch(err){
      if(msg)msg.textContent=err?.message||'Could not preview avatar photo.';
    }
  },
  _cleanBio(user){return userBioText(user);},
  _prefix(user){return userPrefix(user);},
  _parseMute(raw){return parseMuteMeta(raw);},
  _muteLabel(raw){return formatMuteReason(raw)||'Muted right now.';},
  _messageNormalized(text){
    return String(text||'').toLowerCase().replace(/[@4]/g,'a').replace(/[3]/g,'e').replace(/[1!|]/g,'i').replace(/[0]/g,'o').replace(/[$5]/g,'s').replace(/[7]/g,'t').replace(/[8]/g,'b').replace(/[^a-z]/g,'').replace(/(.)\1+/g,'$1');
  },
  _containsProfanity(text){
    const normalized=this._messageNormalized(text);
    const patterns=[
      /b(i|y)t(c|k)h?/,
      /fu?ck/,
      /shit/,
      /asshole/,
      /bastard/,
      /motherfucker/,
      /dick/,
      /cunt/,
      /slut/,
      /whore/,
      /nigger/,
      /niga/,
      /retard/
    ];
    return patterns.some(pattern=>pattern.test(normalized));
  },
  async _ensureSystemChannels(){
    if(!this._requireDb(false))return;
    const required=[
      {id:'announcements',name:'# announcements',description:'Important server updates. Only moderators and owners can post here.',type:'public',category:'CHANNELS',position:0},
      {id:'votes',name:'# 🗳️ votes',description:'Official polls and votes. Only moderators can create polls; everyone can vote.',type:'public',category:'CHANNELS',position:1},
      {id:'forum-hub',name:'# forum',description:'Structured discussions, feedback and topic threads.',type:'forum',category:'FORUM',position:2}
    ];
    if(this.isStaff())required.push(
      {id:'staff-briefing',name:'# staff-briefing',description:'Private room only for moderators and owners.',type:'mod',category:'MOD SERVER',position:3},
      {id:'staff-reports',name:'# staff-reports',description:'Handle reports, warnings and private moderator notes.',type:'mod',category:'MOD SERVER',position:4}
    );
    for(const item of required){
      const{data:exists}=await sb.from('chaty_channels').select('id').eq('id',item.id).single();
      if(!exists)await sb.from('chaty_channels').insert({...item,created_by:this._session?.id||'system'});
      else if(item.id==='votes')await sb.from('chaty_channels').update({name:item.name,description:item.description,category:item.category,type:item.type,position:item.position}).eq('id',item.id);
    }
  },
  async _getActiveWarnings(uid){
    if(!this._requireDb(false))return[];
    const {data:logs}=await sb.from('chaty_mod_log').select('action,reason,created_at,mod_id').eq('target_id',uid).in('action',['WARN','UNWARN']).order('created_at',{ascending:true}).limit(100);
    const active=[];
    for(const log of(logs||[])){
      if(log.action==='WARN')active.push(log);
      if(log.action==='UNWARN'&&active.length)active.pop();
    }
    return active;
  },
  _renderWarningReasons(items){
    if(!(items||[]).length)return `<div class="pf-warning-item">No active warning reasons right now.</div>`;
    return items.map(item=>`<div class="pf-warning-item"><strong>${new Date(item.created_at).toLocaleDateString()}</strong><div style="margin-top:4px">${esc(item.reason||'No reason given.')}</div></div>`).join('');
  },
  async _syncExpiredMutes(users=[]){
    if(!this._requireDb(false))return;
    const pool=(users||[]).filter(Boolean);
    for(const user of pool){
      if(!user?.muted)continue;
      const parsed=this._parseMute(user.mute_reason);
      if(!parsed.until||parsed.until.getTime()>Date.now())continue;
      if(!this.isStaff()&&user.id!==this._session?.id)continue;
      await sb.from('chaty_users').update({muted:false,mute_reason:null}).eq('id',user.id);
      await sb.from('chaty_mod_log').insert({action:'AUTO_UNMUTE',target_id:user.id,mod_id:this._session?.id||'system',reason:'Mute timer expired'});
      if(this._me?.id===user.id){this._me.muted=false;this._me.mute_reason=null;}
    }
  },
  _requireDb(show=true){
    if(sbReady())return true;
    if(show){
      const authErr=document.getElementById('auth-error');
      if(authErr)authErr.textContent=this._dbMsg();
      else alert(this._dbMsg());
    }
    return false;
  },
  _authState(){
    try{return JSON.parse(localStorage.getItem(this._authKey)||'{"fails":0,"lockedUntil":0}');}
    catch{return{fails:0,lockedUntil:0};}
  },
  _saveAuthState(state){localStorage.setItem(this._authKey,JSON.stringify(state));},
  _recordAuthFailure(){
    const state=this._authState();
    const now=Date.now();
    state.fails=(state.fails||0)+1;
    if(state.fails>=5){state.lockedUntil=now+30000;state.fails=0;}
    this._saveAuthState(state);
    return state.lockedUntil&&state.lockedUntil>now?Math.ceil((state.lockedUntil-now)/1000):0;
  },
  _clearAuthFailures(){localStorage.removeItem(this._authKey);},
  _authLockLeft(){
    const state=this._authState();
    const now=Date.now();
    return state.lockedUntil&&state.lockedUntil>now?Math.ceil((state.lockedUntil-now)/1000):0;
  },
  _normalizeText(v){return String(v||'').replace(/\s+/g,' ').trim().toLowerCase();},
  _serverCard(users=this._lastUsers,chs=this._lastChannels){
    const publicCount=(chs||[]).filter(c=>c.type==='public').length;
    const staffCount=(users||[]).filter(u=>u.role==='owner'||u.role==='mod').length;
    return `<div class="dc-server-name">DIHCORD</div><div class="dc-server-sub">School server for study, memes and quick help. Built for a growing student community.</div><div class="dc-stats-row"><div class="dc-stat-pill"><div class="dc-stat-num">${(users||[]).length}</div><div class="dc-stat-lbl">Users</div></div><div class="dc-stat-pill"><div class="dc-stat-num">${publicCount}</div><div class="dc-stat-lbl">Channels</div></div><div class="dc-stat-pill"><div class="dc-stat-num">${staffCount}</div><div class="dc-stat-lbl">Staff</div></div></div>`;
  },
  setChannelFilter(v){this._channelFilter=(v||'').trim().toLowerCase();this.loadChs();},
  setMemberFilter(v){this._memberFilter=(v||'').trim().toLowerCase();this._loadMembers();},
  _slashCommand(text){
    if(!text.startsWith('/'))return null;
    const raw=text.slice(1).trim();
    const [rawCmd,...rest]=raw.split(' ');
    const cmd=(rawCmd||'').toLowerCase();
    const arg=rest.join(' ').trim();
    if(cmd==='shrug')return arg?`${arg} ¯\\_(ツ)_/¯`:`¯\\_(ツ)_/¯`;
    if(cmd==='tableflip')return '(╯°□°)╯︵ ┻━┻';
    if(cmd==='unflip')return '┬─┬ ノ( ゜-゜ノ)';
    if(cmd==='me')return arg?`* ${this._session?.name||'user'} ${arg}`:null;
    if(cmd==='wave')return arg?`o/ ${arg}`:'o/';
    if(cmd==='lenny')return '( ͡° ͜ʖ ͡°)';
    if(cmd==='greet')return arg?`Hello, ${arg}!`:'Hello, everyone!';
    if(cmd==='roll'){const max=Math.min(999,Math.max(2,Number(rest[0])||100));return `rolled 1-${max}: ${Math.floor(Math.random()*max)+1}`;}
    if(cmd==='coin')return `coin flip: ${Math.random()<.5?'heads':'tails'}`;
    if(cmd==='8ball'){const picks=['Yes.','No.','Ask later.','Very likely.','Not happening.','Maybe.'];return arg?`8ball: ${picks[Math.floor(Math.random()*picks.length)]}`:'Ask a question first.';}
    if(cmd==='choose'){const picks=arg.split('|').map(v=>v.trim()).filter(Boolean);return picks.length?`choose: ${picks[Math.floor(Math.random()*picks.length)]}`:'Use /choose a | b | c';}
    if(cmd==='topic')return arg?`Topic: ${arg}`:'Use /topic <text>';
    if(cmd==='poll'){const bits=arg.split('|').map(v=>v.trim()).filter(Boolean);if(bits.length<3)return 'Use /poll Question | Option 1 | Option 2';return{type:'poll',question:bits[0],options:bits.slice(1,9)};}
    if(cmd==='spoiler')return arg?`[spoiler] ${arg}`:null;
    if(cmd==='help')return 'Commands: /shrug, /tableflip, /unflip, /me <text>, /wave, /lenny, /greet, /roll [max], /coin, /8ball <question>, /choose a | b, /topic <text>, /poll Question | A | B, /spoiler <text>';
    return '__unknown__';
  },
  _messageGuard(text){
    const normalized=this._normalizeText(text);
    if(!normalized)return{ok:false,msg:'Message is empty.'};
    if(text.length>this._maxMessageLength)return{ok:false,msg:`Message is too long. Max ${this._maxMessageLength} characters.`};
    if(/(.)\1{14,}/.test(text))return{ok:false,msg:'Too many repeated characters.'};
    if(text.length>18&&text===text.toUpperCase()&&/[A-ZА-ЯЁ]/.test(text))return{ok:false,msg:'Too much CAPS. Relax a bit.'};
    if(this._blockedWords.some(word=>normalized.includes(word)))return{ok:false,msg:'That message looks unsafe for a school chat.'};
    if(this._containsProfanity(text))return{ok:false,msg:'English profanity is blocked in this server.'};
    if(this._riskyDomains.some(domain=>normalized.includes(domain)))return{ok:false,msg:'That link is blocked as risky.'};
    return{ok:true};
  },
  _closeLiveSubs(){if(this._sub&&sbReady()){sb.removeChannel(this._sub);this._sub=null;}if(this._tsub&&sbReady()){sb.removeChannel(this._tsub);this._tsub=null;}},
  _warningInfo(user){
    const warnings=Math.max(0,Number(user?.warnings)||0);
    if(user?.banned)return{tone:'warn-bad',title:'BANNED',detail:user?.ban_reason||'Your access is blocked right now.',count:warnings};
    if(user?.muted)return{tone:'warn-warn',title:'MUTED',detail:this._muteLabel(user?.mute_reason)||'You can read, but you cannot send messages right now.',count:warnings};
    if(warnings>=3)return{tone:'warn-bad',title:`${warnings} WARNINGS`,detail:'Your account is close to bigger moderation action. Keep it clean.',count:warnings};
    if(warnings>0)return{tone:'warn-warn',title:`${warnings} WARNING${warnings===1?'':'S'}`,detail:'Warnings are now visible to you here. Slow down and follow the server rules.',count:warnings};
    return{tone:'warn-good',title:'CLEAN',detail:'No active warnings on your account.',count:0};
  },
  _warningChip(user){
    const info=this._warningInfo(user);
    return `<span class="warn-chip ${info.tone}">${esc(info.title)}</span>`;
  },
  _renderUserPanel(user){
    const s=this._session||{};
    const current=user||this._me||{};
    const color=current.avatar_color||s.color||'#5e8ed6';
    const adminBtn=this.isStaff()?'<button class="dc-theme-btn" onclick="App.goAdmin()" title="Admin Panel">ADM</button>':'';
    document.getElementById('ch-user').innerHTML=`${this._avatarHtml(current,color,'dc-user-av',s.id)}<div class="dc-user-info"><div class="dc-user-nm">${esc(this._displayName(current,s.id||'user'))}</div><div class="dc-user-id">@${esc(s.id||current.id||'')}</div><div class="dc-user-standing">${this._warningChip(current)}</div></div><div class="dc-user-actions"><button class="dc-theme-btn" onclick="App.toggleTheme()">${this._theme==='light'?'🌙':'☀️'}</button>${adminBtn}<button class="dc-logout" onclick="App.logout()">⏻</button></div>`;
  },
  async goHome(){
    this.page='home';this.ch=null;this.replyTo=null;this._closeLiveSubs();
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
    document.getElementById('nav-home')?.classList.add('dc-active');
    document.getElementById('dc-members')?.classList.add('hidden');
    const users=this._lastUsers||[];
    const channels=this._lastChannels||[];
    const me=this._me||{};
    const standing=this._warningInfo(me);
    const publicChannels=channels.filter(c=>c.type==='public').slice(0,6);
    document.getElementById('chat-area').innerHTML=`<div class="dc-home"><div class="dc-home-hero"><div class="dc-home-kicker">School Server</div><div class="dc-home-title">Welcome to DIHCORD</div><div class="dc-home-text">A bigger student chat needs clearer navigation, better protection and faster tools. This version adds smarter filters, reports, safer posting and a cleaner server home.</div></div><div class="dc-home-grid"><div class="dc-home-card"><h3>Community Snapshot</h3><p>${users.length} accounts, ${publicChannels.length||channels.filter(c=>c.type==='public').length} public rooms and growing activity across the school.</p><div class="dc-home-list"><div class="dc-home-link"><span>Active accounts</span><strong>${users.length}</strong></div><div class="dc-home-link"><span>Staff team</span><strong>${users.filter(u=>u.role==='owner'||u.role==='mod').length}</strong></div><div class="dc-home-link"><span>Protected mode</span><strong>ON</strong></div></div></div><div class="dc-home-card"><h3>Quick Rules</h3><p>Keep it school-safe, avoid spam, don’t post risky links, and report toxic or suspicious messages right from chat.</p><div class="dc-home-list"><div class="dc-home-link"><span>No spam floods</span><strong>✓</strong></div><div class="dc-home-link"><span>No risky links</span><strong>✓</strong></div><div class="dc-home-link"><span>Easy report tool</span><strong>✓</strong></div></div></div><div class="dc-home-card"><h3>Popular Channels</h3><p>Jump into the most important rooms from here.</p><div class="dc-home-list">${publicChannels.map(c=>`<div class="dc-home-link" onclick='App.openChat(${q(c.id)})'><span>${esc(c.name.replace(/^#\s*/,''))}</span><strong>#</strong></div>`).join('')||'<div class="dc-home-link"><span>No public channels yet</span><strong>-</strong></div>'}</div></div></div></div>`;
  },
  _composerEls(){return{input:document.getElementById('chat-input'),limit:document.getElementById('dc-input-limit'),note:document.getElementById('dc-input-note')};},
  _setComposerState(msg='',tone=''){
    const{note}=this._composerEls();
    if(!note)return;
    note.textContent=msg;
    note.className='dc-input-note'+(tone==='error'?' dc-note-error':tone==='warn'?' dc-note-warn':'');
  },
  _updateComposerMeta(){
    const{input,limit}=this._composerEls();
    if(!input||!limit)return;
    const left=this._maxMessageLength-input.value.length;
    limit.textContent=`${Math.max(left,0)} chars left`;
    limit.className='dc-input-limit'+(left<60&&left>=20?' dc-limit-warn':left<20?' dc-limit-bad':'');
  },
  _trimSendWindows(now=Date.now()){
    this._recentSends=this._recentSends.filter(ts=>now-ts<this._windowMs);
  },
  async _canSendMessage(text){
    const now=Date.now();
    const normalized=text.replace(/\s+/g,' ').trim().toLowerCase();
    this._trimSendWindows(now);
    if(now<this._cooldownUntil)return{ok:false,msg:`Slow down. Try again in ${Math.ceil((this._cooldownUntil-now)/1000)}s.`};
    if(text.length>this._maxMessageLength)return{ok:false,msg:`Message is too long. Max ${this._maxMessageLength} characters.`};
    if(now-this._lastSendAt<this._minSendGapMs)return{ok:false,msg:'You are sending too fast.'};
    const burstCount=this._recentSends.filter(ts=>now-ts<this._burstMs).length;
    if(burstCount>=this._burstLimit){this._cooldownUntil=now+6000;return{ok:false,msg:'Too many messages in a row. Wait 6s.'};}
    if(this._recentSends.length>=this._rateLimit){const oldest=this._recentSends[0];return{ok:false,msg:`Rate limit hit. Wait ${Math.ceil((this._windowMs-(now-oldest))/1000)}s.`};}
    try{
      const since=new Date(now-this._windowMs).toISOString();
      const {data,error}=await withTimeout(sb.from('chaty_messages').select('id,created_at,content').eq('channel_id',this.ch).eq('user_id',this._session.id).gte('created_at',since).order('created_at',{ascending:false}).limit(this._rateLimit),4000,'Spam check');
      if(!error&&Array.isArray(data)&&data.length>=this._rateLimit)return{ok:false,msg:'Rate limit hit. Wait a moment.'};
      if(!error&&Array.isArray(data)&&data.some(m=>String(m.content||'').replace(/\s+/g,' ').trim().toLowerCase()===normalized))return{ok:false,msg:'Do not send the same message again and again.'};
    }catch{}
    return{ok:true};
  },
  showAuth(){document.getElementById('auth-screen').classList.remove('hidden');document.getElementById('app').classList.add('hidden');document.getElementById('auth-error').textContent='';setTimeout(()=>document.getElementById('auth-screen').classList.add('visible'),50);this._applySiteLockState();},
  authTab(m){this.mode=m;document.querySelectorAll('.auth-tab').forEach((t,i)=>t.classList.toggle('active',i===(m==='login'?0:1)));document.getElementById('auth-btn').textContent=m==='login'?'LOG IN':'REGISTER';document.getElementById('auth-error').textContent='';},

  async handleAuth(){
    if(!this._requireDb())return;
    const btn=document.getElementById('auth-btn');btn.disabled=true;btn.textContent='...';
    const user=document.getElementById('auth-user').value.trim().toLowerCase(),pass=document.getElementById('auth-pass').value,err=document.getElementById('auth-error');
    const lockedFor=this._authLockLeft();
    if(lockedFor>0){err.textContent='Too many login tries. Wait '+lockedFor+'s';btn.disabled=false;btn.textContent=this.mode==='login'?'LOG IN':'REGISTER';return;}
    if(!user||!pass||user.length<3){err.textContent=!user||!pass?'Fill all fields':'3+ chars';btn.disabled=false;btn.textContent=this.mode==='login'?'LOG IN':'REGISTER';return;}
    if(!/^[a-z0-9_-]{3,24}$/.test(user)){err.textContent='Use 3-24 letters, numbers, _ or -';btn.disabled=false;btn.textContent=this.mode==='login'?'LOG IN':'REGISTER';return;}
    if(pass.length<4||pass.length>this._maxPasswordLength){err.textContent='Password must be 4-'+this._maxPasswordLength+' chars';btn.disabled=false;btn.textContent=this.mode==='login'?'LOG IN':'REGISTER';return;}
    try{
      if(this.mode==='register'){
        const f=fp();const{data:ex}=await sb.from('chaty_users').select('id').eq('device_fingerprint',f).single();
        if(ex){err.textContent='One account per PC. Yours: '+ex.id;btn.disabled=false;btn.textContent='REGISTER';return;}
        const{data:tk}=await sb.from('chaty_users').select('id').eq('id',user).single();
        if(tk){err.textContent='Taken';btn.disabled=false;btn.textContent='REGISTER';return;}
        const color=randColor();
        const{error}=await sb.from('chaty_users').insert({id:user,password:pass,display_name:user,avatar_color:color,device_fingerprint:f,role:'user'});
        if(error){err.textContent=error.message;btn.disabled=false;btn.textContent='REGISTER';return;}
        this._clearAuthFailures();
        this._session={id:user,name:user,color,role:'user'};localStorage.setItem('chaty_session',JSON.stringify(this._session));this.showApp();
      } else {
        const{data:u}=await sb.from('chaty_users').select('*').eq('id',user).single();
        if(!u){const wait=this._recordAuthFailure();err.textContent=wait>0?'Too many tries. Wait '+wait+'s':'Not found';btn.disabled=false;btn.textContent='LOG IN';return;}
        if(u.password!==pass){const wait=this._recordAuthFailure();err.textContent=wait>0?'Too many tries. Wait '+wait+'s':'Wrong password';btn.disabled=false;btn.textContent='LOG IN';return;}
        if(u.banned){err.textContent='BANNED'+(u.ban_reason?': '+u.ban_reason:'');btn.disabled=false;btn.textContent='LOG IN';return;}
        this._clearAuthFailures();
        this._session={id:u.id,name:u.display_name||u.id,color:u.avatar_color,role:u.role||'user'};
        localStorage.setItem('chaty_session',JSON.stringify(this._session));this.showApp();
      }
    }catch(e){
      err.textContent=e?.message||'Auth failed';
    }
    btn.disabled=false;
  },

  logout(){const sid=this._session?.id;if(sbReady())[this._sub,this._tsub,this._inboxSub].forEach(s=>{if(s)sb.removeChannel(s)});this._sub=this._tsub=this._inboxSub=null;clearTimeout(this._typingTimer);this.page='chat';this.ch=null;this.replyTo=null;this._role='user';this._me=null;this._cache={};this._session=null;this.clearPendingUpload();if(sbReady()&&sid)sb.from('chaty_typing').delete().eq('user_id',sid).then(()=>{});localStorage.removeItem('chaty_session');document.getElementById('app').classList.add('hidden');this.showAuth();},
  isStaff(){
    const roles=[this._role,this._session?.role,this._me?.role,this._cache?.[this._session?.id]?.role].map(v=>String(v||'').trim().toLowerCase());
    const ids=[this._session?.id,this._session?.name,this._me?.id,this._me?.display_name].map(v=>String(v||'').trim().toLowerCase());
    const staffRoles=['owner','mod','admin','moderator','staff'];
    return roles.some(role=>staffRoles.includes(role))||ids.some(id=>id===this._siteLockOwnerId||id.includes('mrkotyvell'));
  },

  async showApp(){
    if(!this._requireDb()){this.showAuth();document.getElementById('auth-error').textContent=this._dbMsg();return;}
    document.getElementById('auth-screen').classList.add('hidden');document.getElementById('auth-screen').classList.remove('visible');document.getElementById('app').classList.remove('hidden');
    const{data:me}=await sb.from('chaty_users').select('*').eq('id',this._session.id).single();
    if(!me){this.logout();return;}
    await this._syncExpiredMutes([me]);
    this._me=me;this._role=me.role||'user';this._session.role=this._role;this._session.name=me.display_name||me.id;this._session.color=me.avatar_color||this._session.color;localStorage.setItem('chaty_session',JSON.stringify(this._session));
    if(me?.banned){alert('You are banned'+(me.ban_reason?': '+me.ban_reason:''));this.logout();return;}
    await this._ensureSystemChannels();
    this._requestNotifyPermission();
    this._renderUserPanel(me);
    this._syncNavShell();
    this._renderNav();
    this._setupSystemSub();
    await this._refreshSiteLockState();
    await this._refreshHomeNewsState();
    await this.loadChs();
    this._setupInboxSub();
    this.goHome();
  },

  async loadChs(force=false){
    if(!this._requireDb())return;
    const now=Date.now();
    if(this._loadingChs){this._queuedLoadChs=true;return;}
    if(!force&&this._lastLoadChsAt&&now-this._lastLoadChsAt<1200){this._scheduleLoadChs(1200-(now-this._lastLoadChsAt));return;}
    this._loadingChs=true;
    this._lastLoadChsAt=now;
    try{
    const{data:chs}=await sb.from('chaty_channels').select('*').order('position');const s=this._session;
    this._lastChannels=chs||[];
    const retiredBridge=(chs||[]).filter(c=>this._isRetiredBridgeChannel(c)),pub=(chs||[]).filter(c=>c.type==='public'&&!this._isRetiredBridgeChannel(c)),forum=(chs||[]).filter(c=>c.type==='forum'),modOnly=(chs||[]).filter(c=>c.type==='mod'),dms=(chs||[]).filter(c=>c.type==='dm'&&(c.members||[]).includes(s.id));
    const{data:users}=await sb.from('chaty_users').select('id,display_name,avatar_color,role,banned,muted,mute_reason,user_status,bio,warnings,created_at');await this._syncExpiredMutes(users||[]);this._lastUsers=users||[];(users||[]).forEach(u=>this._cache[u.id]=u);
    document.getElementById('dc-server-card').innerHTML=this._serverCard(users||[],chs||[]);
    const others=(users||[]).filter(u=>u.id!==s.id);
    const filter=this._channelFilter;
    let dmLastMap={},dmMeta={...this._dmMeta};
    if(dms.length){
      const dmIds=dms.map(c=>c.id);
      try{
        const {data:dmMsgs}=await sb.from('chaty_messages').select('channel_id,created_at,content,user_id,user_name').in('channel_id',dmIds).order('created_at',{ascending:false}).limit(Math.min(Math.max(dmIds.length*6,24),120));
        for(const row of(dmMsgs||[]))if(dmLastMap[row.channel_id]===undefined){dmLastMap[row.channel_id]=new Date(row.created_at).getTime();dmMeta[row.channel_id]={ts:new Date(row.created_at).getTime(),content:row.content||'',user_id:row.user_id||'',user_name:row.user_name||''};}
      }catch{}
    }
    this._dmMeta=dmMeta;
    const sortedDms=[...dms].sort((a,b)=>{
      const aTs=dmLastMap[a.id]||0,bTs=dmLastMap[b.id]||0;
      if(bTs!==aTs)return bTs-aTs;
      const aUser=this._cache[(a.members||[]).find(m=>m!==s.id)];
      const bUser=this._cache[(b.members||[]).find(m=>m!==s.id)];
      return this._displayName(aUser||{id:a.id,display_name:a.id},a.id).localeCompare(this._displayName(bUser||{id:b.id,display_name:b.id},b.id));
    });
    const votesChannel=pub.find(c=>c.id==='votes');
    const voteTop=votesChannel&&(!filter||`${votesChannel.name} ${votesChannel.description||''}`.toLowerCase().includes(filter))?votesChannel:null;
    const pubFiltered=pub.filter(c=>c.id!=='votes'&&(!filter||`${c.name} ${c.description||''}`.toLowerCase().includes(filter)));
    const pinnedBridgeFiltered=retiredBridge.filter(c=>!filter||`${c.name} ${c.description||''}`.toLowerCase().includes(filter));
    const forumFiltered=forum.filter(c=>!filter||`${c.name} ${c.description||''}`.toLowerCase().includes(filter));
    const modFiltered=modOnly.filter(c=>this.isStaff()&&(!filter||`${c.name} ${c.description||''}`.toLowerCase().includes(filter)));
    const dmFiltered=sortedDms.filter(c=>{const o=(c.members||[]).find(m=>m!==s.id);const u=this._cache[o];const label=this._displayName(u||{id:o,display_name:o},'?');return !filter||label.toLowerCase().includes(filter);});
    const othersFiltered=others.filter(u=>!filter||`${this._displayName(u,u.id)} ${u.id}`.toLowerCase().includes(filter));
    const favoriteFiltered=(this._favoriteChannels()||[]).filter(c=>!filter||`${c.name} ${c.description||''}`.toLowerCase().includes(filter));
    let h='';
    if(voteTop)h+=`<div class="dc-ch-item dc-vote-hot" data-id="${attr(voteTop.id)}" onclick='App.openChat(${q(voteTop.id)})'><span class="dc-hash">🗳️</span><div class="dc-dm-copy"><span class="dc-dm-name">${esc(voteTop.name.replace(/^#\s*/,''))}</span><span class="dc-dm-preview">Polls only • vote here</span></div></div>`;
    if(pinnedBridgeFiltered.length)h+=`<div class="dc-cat"><div class="dc-cat-title">PINNED CHAT</div>${pinnedBridgeFiltered.map(c=>`<div class="dc-ch-item" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'><span class="dc-hash">#</span><span>${esc(c.name.replace(/^#\s*/,''))}</span></div>`).join('')}</div>`;
    if(favoriteFiltered.length)h+=`<div class="dc-cat"><div class="dc-cat-title">★ FAVORITES</div>${favoriteFiltered.map(c=>`<div class="dc-ch-item dc-fav" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'><span class="dc-hash">${this._channelGlyph(c)}</span><span>${esc(c.name.replace(/^#\s*/,''))}</span></div>`).join('')}</div>`;
    if(forumFiltered.length)h+=`<div class="dc-cat"><div class="dc-cat-title">🧵 FORUM</div>${forumFiltered.map(c=>`<div class="dc-ch-item" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'><span class="dc-hash">🧵</span><span>${esc(c.name.replace(/^#\s*/,''))}</span></div>`).join('')}</div>`;
    if(modFiltered.length)h+=`<div class="dc-cat"><div class="dc-cat-title">🛡 MOD SERVER</div>${modFiltered.map(c=>`<div class="dc-ch-item" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'><span class="dc-hash">🛡</span><span>${esc(c.name.replace(/^#\s*/,''))}</span></div>`).join('')}</div>`;
    h+=`<div class="dc-cat"><div class="dc-cat-title" onclick="this.parentElement.classList.toggle('dc-cat-collapsed')">CHANNELS</div>${pubFiltered.map(c=>`<div class="dc-ch-item" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'><span class="dc-hash">#</span><span>${esc(c.name.replace(/^#\s*/,''))}</span></div>`).join('')||'<div class="dc-ch-add">No matching channels</div>'}<div class="dc-ch-add" onclick="App.showNewCh()">+ New Channel</div></div>`;
    if(dmFiltered.length||othersFiltered.length){h+=`<div class="dc-cat"><div class="dc-cat-title" onclick="this.parentElement.classList.toggle('dc-cat-collapsed')">DIRECT MESSAGES</div>`;h+=dmFiltered.map(c=>{const o=(c.members||[]).find(m=>m!==s.id);const u=this._cache[o];const label=this._displayName(u||{id:o,display_name:o},'?');const unread=this._unreadCount(c.id);const meta=this._dmMeta[c.id]||{};const preview=this._settings.dmPreviews!==false?(meta.content?(meta.user_id===s.id?`You: ${this._rawContentPreview(meta.content,28)}`:this._rawContentPreview(meta.content,32)):'No messages yet'):label;const time=this._relativeTime(meta.ts);return`<div class="dc-ch-item ${unread?'dc-unread':''}" data-id="${attr(c.id)}" onclick='App.openChat(${q(c.id)})'>${this._avatarHtml(u||{id:o,display_name:o},u?u.avatar_color:'#5e8ed6','dc-dm-av','?')}<div class="dc-dm-meta"><div class="dc-dm-copy"><span class="dc-dm-name">${esc(label)}</span><span class="dc-dm-preview">${esc(preview)}</span></div><div class="dc-dm-side">${time?`<span class="dc-dm-time">${esc(time)}</span>`:''}${unread?`<span class="dc-unread-badge">${unread>99?'99+':unread}</span>`:''}</div></div></div>`;}).join('');h+=othersFiltered.map(u=>`<div class="dc-ch-item dc-dm-start" onclick='App.startDm(${q(u.id)})'>${this._avatarHtml(u,u.avatar_color||'#5e8ed6','dc-dm-av',u.id)}<span>${esc(this._displayName(u,u.id))}</span></div>`).join('');h+=`</div>`;}
    document.getElementById('ch-list').innerHTML=h;
    if(this.page==='chat'&&this.ch)byDataId(this.ch)?.classList.add('dc-active');
    }finally{
      this._loadingChs=false;
      if(this._queuedLoadChs){
        this._queuedLoadChs=false;
        this._scheduleLoadChs(250);
      }
    }
  },

  /* ===== CHAT ===== */
  async openChat(chId){
    if(!this._requireDb())return;
    this.page='chat';this.ch=chId;this.replyTo=null;
    this._liveTrafficHits=[];
    this._liveTrafficUntil=0;
    this._liveTrafficDropped=0;
    clearTimeout(this._liveTrafficTimer);
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
    byDataId(chId)?.classList.add('dc-active');
    const{data:ch,error:chError}=await sb.from('chaty_channels').select('*').eq('id',chId).single();
    if(chError||!ch){document.getElementById('chat-area').innerHTML=`<div class="dc-main-empty"><div class="dc-empty-icon">!</div><div>Channel failed to load</div></div>`;return;}
    const retiredBridge=this._isRetiredBridgeChannel(ch);
    const isBr=false,isDm=ch?.type==='dm',isModRoom=ch?.type==='mod',isForum=ch?.type==='forum'&&!retiredBridge,isAnnouncements=ch?.id==='announcements',isVotes=ch?.id==='votes';
    if(isModRoom&&!this.isStaff()){document.getElementById('chat-area').innerHTML=`<div class="dc-main-empty"><div class="dc-empty-icon">🛡</div><div>This room is only for moderators.</div></div>`;return;}
    if(isForum){await this._openForum(ch);return;}
    let name=ch?ch.name.replace(/^#\s*/,''):chId;
    if(isDm){const o=(ch.members||[]).find(m=>m!==this._session.id);const u=this._cache[o];name=this._displayName(u||{id:o,display_name:o},o);}
    if(isDm){this._markRead(chId);const activeItem=byDataId(chId);activeItem?.classList.remove('dc-unread');activeItem?.querySelector('.dc-unread-badge')?.remove();}
    const isMuted=this._me?.muted;
    const channelMuted=this._isChannelMuted(chId);
    const isReadOnlyAnnouncements=isAnnouncements&&!this.isStaff();
    const isReadOnlyVotes=isVotes&&!this.isStaff();
    const isReadOnlyChannel=isReadOnlyAnnouncements||isReadOnlyVotes;
    const draftText=this._draftFor(chId);
    const safeName=esc(name);
    const safeDesc=esc(retiredBridge?'Alyon Bridge is retired. This is now a normal pinned chat; old messages stay here.':(ch?.description||'Start chatting!'));
    const baseComposerNote=channelMuted?'Local mute active for this room. Alerts stay silent on this device.':`Anti-spam on • Max ${this._maxMessageLength} chars • ${this._rateLimit} msgs / ${Math.round(this._windowMs/1000)}s`;

    const area=document.getElementById('chat-area');
    const canFavorite=!isDm;
    area.innerHTML=`<div class="dc-header"><span class="dc-h-icon">${isBr?'🌉':isDm?'@':isModRoom?'🛡':'#'}</span><span class="dc-h-name">${safeName}</span>${isBr?'<span class="dc-h-tag">ALYON ↔ CHATY</span>':''}${isModRoom?'<span class="dc-h-tag">STAFF ONLY</span>':''}${(retiredBridge||ch?.description)&&!isDm?`<span style="color:var(--border);margin:0 6px">|</span><span class="dc-h-desc">${safeDesc}</span>`:''}<div class="dc-h-actions">${canFavorite?`<button class="dc-h-btn ${this._isFavorite(chId)?'active':''}" id="dc-fav-btn" onclick='App.toggleFavorite(${q(chId)})' title="${this._isFavorite(chId)?'Remove from favorites':'Add to favorites'}"><span>★</span><span>${this._isFavorite(chId)?'Starred':'Star'}</span></button>`:''}<button class="dc-h-btn ${channelMuted?'active':''}" id="dc-mute-btn" onclick='App.toggleChannelMute(${q(chId)})' title="${channelMuted?'Unmute local alerts':'Mute local alerts'}"><span>${channelMuted?'OFF':'M'}</span><span>${channelMuted?'Muted':'Mute'}</span></button><button class="dc-h-btn" onclick="App.showSearchPanel()"><span>🔎</span><span>Search</span></button><button class="dc-h-btn" onclick="App.showPins()"><span>📌</span><span>Pins</span></button><button class="dc-h-btn" onclick="App.toggleMembers()"><span>👥</span><span>People</span></button></div></div>
      <div class="dc-msgs" id="dc-msgs"><div class="dc-welcome"><div class="dc-welcome-icon">${isBr?'🌉':isModRoom?'🛡':'#'}</div><div class="dc-welcome-title">${isBr?'Alyon ↔ Chaty Bridge':isModRoom?'Welcome to the moderator server':'Welcome to #'+safeName+'!'}</div><div class="dc-welcome-desc">${safeDesc}</div></div><div id="dc-history-tools" class="hidden" style="padding:0 8px 8px"><button class="btn btn-outline" id="dc-load-older" onclick="App.loadOlderMsgs()" style="width:100%">Load older messages</button></div><div id="dc-msg-list"></div></div>
      <div id="dc-reply-bar" class="dc-reply-bar hidden"></div>
      <div id="dc-typing" class="dc-typing"></div>
      ${isMuted?`<div class="dc-muted-bar">🔇 You are muted${this._me.mute_reason?' — '+esc(this._muteLabel(this._me.mute_reason)):''}</div>`:`
      <div class="dc-input-area"><div class="dc-input-shell"><div class="dc-input-wrap"><button type="button" id="chat-file-btn" class="dc-input-btn" onclick="App.pickImage()" title="Upload image">+</button><input type="file" id="chat-file" class="hidden" accept="image/png,image/jpeg,image/webp,image/gif" onchange="App.handleImagePick(this)"><input type="text" id="chat-input" class="dc-input" maxlength="${this._maxMessageLength}" placeholder="Message ${isDm?'@':'#'}${safeName}" autocomplete="off"></div><div id="dc-upload-preview" class="dc-upload-preview hidden"></div><div class="dc-input-meta"><div id="dc-input-note" class="dc-input-note">${baseComposerNote}</div><div id="dc-input-limit" class="dc-input-limit">${this._maxMessageLength} chars left</div></div></div></div>`}`;

    if(isVotes){
      const hIcon=area.querySelector('.dc-h-icon');
      const hName=area.querySelector('.dc-h-name');
      const wIcon=area.querySelector('.dc-welcome-icon');
      const wTitle=area.querySelector('.dc-welcome-title');
      const actions=area.querySelector('.dc-h-actions');
      if(hIcon)hIcon.textContent='🗳️';
      if(hName)hName.insertAdjacentHTML('afterend','<span class="dc-h-tag">VOTES</span>');
      if(wIcon)wIcon.textContent='🗳️';
      if(wTitle)wTitle.textContent='Welcome to #votes!';
      if(actions&&this.isStaff())actions.insertAdjacentHTML('afterbegin','<button class="dc-h-btn" onclick="App.focusVotePollMaker()"><span>🗳️</span><span>New Poll</span></button>');
      if(this.isStaff()){
        const panel=document.createElement('div');
        panel.className='form-block';
        panel.id='vote-poll-maker';
        panel.style.margin='12px 16px 8px';
        panel.innerHTML=`<div class="form-title">🗳️ Quick Poll Creator</div><div class="form-grid"><div><label class="form-label">Question</label><input id="vote-q" class="form-input" maxlength="120" placeholder="What should we vote on?"></div><div><label class="form-label">Option 1</label><input id="vote-o1" class="form-input" maxlength="40" placeholder="Yes"></div><div><label class="form-label">Option 2</label><input id="vote-o2" class="form-input" maxlength="40" placeholder="No"></div><div><label class="form-label">Option 3</label><input id="vote-o3" class="form-input" maxlength="40" placeholder="Optional"></div><div><label class="form-label">Option 4</label><input id="vote-o4" class="form-input" maxlength="40" placeholder="Optional"></div></div><div class="site-actions" style="margin-top:12px"><button class="btn btn-accent" onclick="App.createVotePollSimple()">Post Poll</button><button class="btn btn-outline" onclick="App.fillVotePollExample()">Example</button></div><div id="vote-poll-msg" class="admin-msg"></div>`;
        const msgs=area.querySelector('#dc-msgs');
        if(msgs)area.insertBefore(panel,msgs);
        const note=document.getElementById('dc-input-note');
        if(note)note.textContent='Quick creator is above. You can also type /poll Question | Option A | Option B';
      }
    }

    const scrollBox=document.getElementById('dc-msgs');
    const list=document.getElementById('dc-msg-list');
    const s=this._session;
    await this._loadInitialMsgs(chId);
    scrollBox.scrollTop=scrollBox.scrollHeight;

    if(this._sub)sb.removeChannel(this._sub);
    this._sub=sb.channel('ch-'+chId).on('postgres_changes',{event:'*',schema:'public',table:'chaty_messages',filter:'channel_id=eq.'+chId},async p=>{
      if(p.eventType==='INSERT'){
        if(this._registerLiveTraffic()){this._liveTrafficDropped++;return;}
        if(p.new?.user_id)await this._cacheUserById(p.new.user_id);
        const last=list.querySelector('.dc-msg-group:last-child');
        this._addMsg(list,p.new,s.id,last?last.dataset.sender:null,last?+last.dataset.time:0);
        this._trimRenderedMessages();
        scrollBox.scrollTop=scrollBox.scrollHeight;
        if(p.new.user_id!==s.id&&!this._trafficShieldActive()&&!this._isChannelMuted(chId))this._snd();
      }
      if(p.eventType==='UPDATE'){this._scheduleChatRefresh(220);}
      if(p.eventType==='DELETE'){this._removeMsgNode(p.old.id);}
    }).subscribe();

    // Typing subscription
    if(this._tsub)sb.removeChannel(this._tsub);
    this._tsub=sb.channel('typing-'+chId).on('postgres_changes',{event:'*',schema:'public',table:'chaty_typing',filter:'channel_id=eq.'+chId},()=>this._refreshTyping(true)).subscribe();
    this._refreshTyping();

    this._loadMembers();
    if(!isMuted&&isReadOnlyChannel){
      const inp=document.getElementById('chat-input');
      if(inp){
        inp.disabled=true;
        inp.placeholder=isReadOnlyVotes?'Only moderators can create votes here':'Only moderators can post in announcements';
      }
      document.getElementById('chat-file-btn')?.setAttribute('disabled','disabled');
      this._setComposerState(isReadOnlyVotes?'This channel is read-only for members. You can still vote on active polls.':'This channel is read-only for members. Moderators and owners can post announcements.','warn');
      this._updateComposerMeta();
    }
    if(!isMuted&&!isReadOnlyChannel){
      const inp=document.getElementById('chat-input');
      inp.addEventListener('keydown',e=>{if(e.key==='Enter')App.sendMsg();if(e.key==='Escape')App.cancelReply();});
      inp.addEventListener('input',()=>{this._onType();this._setDraft(chId,inp.value);this._updateComposerMeta();if(inp.value.length===0)this._setComposerState(baseComposerNote,channelMuted?'warn':'');});
      if(draftText){
        inp.value=draftText;
        this._setComposerState(channelMuted?'Draft restored. Local mute is still active for this room.':'Draft restored for this room.',channelMuted?'warn':'');
      }else if(channelMuted)this._setComposerState(baseComposerNote,'warn');
      this._updateComposerMeta();
      this._renderPendingUpload();
      inp.focus();
    }
  },

  async _refreshOpenChat(){if(this.page!=='chat'||!this.ch)return;const current=this.ch;await this.openChat(current);},
  _removeMsgNode(id){
    const node=document.querySelector(`[data-msg-id="${id}"]`);
    if(!node)return;
    if(node.classList.contains('dc-msg-compact')){
      const group=node.closest('.dc-msg-group');
      node.remove();
      if(group&&!group.querySelector('[data-msg-id]'))group.remove();
      return;
    }
    this._scheduleChatRefresh(160);
  },
  _historyUi(){
    return{
      box:document.getElementById('dc-msgs'),
      list:document.getElementById('dc-msg-list'),
      tools:document.getElementById('dc-history-tools'),
      btn:document.getElementById('dc-load-older')
    };
  },
  _renderMsgBatch(list,msgs,prepend=false){
    if(!list||!(msgs||[]).length)return;
    const groups=[...list.querySelectorAll('.dc-msg-group')];
    let ls=prepend?null:(groups.pop()?.dataset.sender||null);
    let lt=prepend?0:((()=>{const lastGroup=[...list.querySelectorAll('.dc-msg-group')].pop();return lastGroup?+lastGroup.dataset.time:0;})());
    const frag=document.createDocumentFragment();
    for(const m of(msgs||[])){this._addMsg(frag,m,this._session.id,ls,lt);ls=m.user_id;lt=new Date(m.created_at).getTime();}
    if(prepend)list.prepend(frag);else list.appendChild(frag);
  },
  _updateHistoryUi(){
    const{tools,btn}=this._historyUi();
    if(!tools||!btn)return;
    const show=!this._loadedAllHistory&&!!this._oldestMsgAt;
    tools.classList.toggle('hidden',!show);
    btn.disabled=this._loadingHistory;
    btn.textContent=this._loadingHistory?'Loading...':'Load older messages';
  },
  async _loadInitialMsgs(chId){
    if(!this._requireDb(false))return;
    const{list}=this._historyUi();
    if(!list)return;
    list.innerHTML='';
    this._oldestMsgAt=null;
    this._loadedAllHistory=false;
    let msgs,error;
    try{
      ({data:msgs,error}=await withTimeout(sb.from('chaty_messages').select('id,channel_id,user_id,user_name,content,platform,reply_to,reactions,pinned,edited,created_at').eq('channel_id',chId).order('created_at',{ascending:false}).limit(this._msgPageSize),8000,'Loading chat history'));
    }catch(e){
      error={message:e.message};
    }
    if(error){list.innerHTML=`<div style="padding:16px;color:var(--red);font-family:var(--mono)">Failed to load messages: ${esc(error.message)}</div>`;this._loadedAllHistory=true;this._updateHistoryUi();return;}
    const ordered=(msgs||[]).slice().reverse();
    this._renderMsgBatch(list,ordered,false);
    this._oldestMsgAt=ordered[0]?.created_at||null;
    this._loadedAllHistory=(ordered.length<this._msgPageSize)||!ordered.length;
    this._updateHistoryUi();
  },
  async loadOlderMsgs(){
    if(!this._requireDb(false))return;
    if(this._loadingHistory||this._loadedAllHistory||!this.ch||!this._oldestMsgAt)return;
    const{box,list}=this._historyUi();
    if(!box||!list)return;
    this._loadingHistory=true;
    this._updateHistoryUi();
    const prevHeight=box.scrollHeight;
    let msgs,error;
    try{
      ({data:msgs,error}=await withTimeout(sb.from('chaty_messages').select('id,channel_id,user_id,user_name,content,platform,reply_to,reactions,pinned,edited,created_at').eq('channel_id',this.ch).lt('created_at',this._oldestMsgAt).order('created_at',{ascending:false}).limit(this._msgPageSize),8000,'Loading older messages'));
    }catch(e){
      error={message:e.message};
    }
    this._loadingHistory=false;
    if(error){alert(error.message);this._updateHistoryUi();return;}
    const ordered=(msgs||[]).slice().reverse();
    this._renderMsgBatch(list,ordered,true);
    this._oldestMsgAt=ordered[0]?.created_at||this._oldestMsgAt;
    this._loadedAllHistory=(ordered.length<this._msgPageSize)||!ordered.length;
    this._updateHistoryUi();
    box.scrollTop+=box.scrollHeight-prevHeight;
  },
  _visibleReactions(reactions={}){
    return Object.fromEntries(Object.entries(reactions||{}).filter(([key])=>!key.startsWith('poll:')));
  },
  _messageHtml(m,myId){
    const image=parseImageContent(m?.content||'');
    if(image)return this._renderImageMessage(m);
    const poll=parsePollContent(m?.content||'');
    if(poll)return this._renderPoll(m,myId);
    return rc(m?.content||'');
  },

  _addMsg(c,m,myId,ls,lt){
    const t=new Date(m.created_at),df=t.getTime()-lt,grp=m.user_id===ls&&df<300000;
    const ts=t.toLocaleTimeString([],{hour:'2-digit',minute:'2-digit'}),ds=t.toLocaleDateString([],{month:'short',day:'numeric'});
    if(lt>0&&new Date(lt).toLocaleDateString()!==t.toLocaleDateString()){const d=document.createElement('div');d.className='dc-date-div';d.innerHTML=`<span>${ds}</span>`;c.appendChild(d);}
    const isAlyon=m.platform==='alyon';const user=this._cache[m.user_id];const color=isAlyon?'#c9a84c':(user?user.avatar_color:'#5e8ed6');
    const dn=isAlyon?txt(m.user_name,'?'):this._displayName(user||{id:m.user_id,display_name:stripPrefixLabel(m.user_name)},txt(m.user_name,'?'));const avatarHtml=isAlyon?this._avatarShell(initial(dn),color,'dc-msg-av','none'):this._avatarHtml(user||{id:m.user_id,display_name:stripPrefixLabel(m.user_name)},color,'dc-msg-av',dn);const isMe=m.user_id===myId;const isMod=this.isStaff();
    const role=user?.role||'user';const roleClr={owner:'var(--gold)',mod:'var(--green)'};
    const roleBadge=role&&role!=='user'?`<span class="dc-role-badge" style="background:${roleClr[role]||'#555'}">${role.toUpperCase()}</span>`:'';
    const platBadge=this.ch==='alyon-bridge'?`<span class="dc-plat-badge ${isAlyon?'plat-alyon':'plat-chaty'}">${isAlyon?'ALYON':'CHATY'}</span>`:'';
    const nameClr=isAlyon?'var(--gold)':role==='owner'?'var(--gold)':role==='mod'?'var(--green)':'var(--accent)';
    const reactions=this._visibleReactions(m.reactions||{});const rh=Object.keys(reactions).length?`<div class="dc-reactions">${Object.entries(reactions).map(([e,u])=>`<button class="dc-react-btn ${u.includes(myId)?'dc-react-mine':''}" onclick="App.react(${m.id},'${e}')">${e} ${u.length}</button>`).join('')}</div>`:'';

    if(grp&&!m.reply_to){const last=c.querySelector('.dc-msg-group:last-child');if(last){const body=last.querySelector('.dc-msg-body');const row=document.createElement('div');row.className='dc-msg-row dc-msg-compact';row.dataset.msgId=m.id;row.innerHTML=`<span class="dc-compact-time">${ts}</span><div class="dc-msg-text">${this._messageHtml(m,myId)}</div>${m.edited?'<span class="dc-edited">(edited)</span>':''}${rh}<div class="dc-msg-actions">${this._acts(m,isMe,isMod)}</div>`;body.appendChild(row);last.dataset.time=t.getTime();return;}}
    const g=document.createElement('div');g.className='dc-msg-group';g.dataset.sender=m.user_id;g.dataset.time=t.getTime();
    g.innerHTML=`${avatarHtml}<div class="dc-msg-body"><div class="dc-msg-row" data-msg-id="${m.id}"><span class="dc-msg-author" onclick='App.showProfile(${q(m.user_id)},${q(m.platform||'chaty')})' style="color:${nameClr}">${esc(dn)}</span>${roleBadge}${platBadge}<span class="dc-msg-ts">${ds} ${ts}</span><div class="dc-msg-actions">${this._acts(m,isMe,isMod)}</div></div><div class="dc-msg-row" data-msg-id="${m.id}"><div class="dc-msg-text">${this._messageHtml(m,myId)}</div>${m.edited?'<span class="dc-edited">(edited)</span>':''}</div>${rh}</div>`;
    c.appendChild(g);
  },

  _acts(m,isMe,isMod){const saved=this._isSavedMessage(m.id);let a=`<button class="dc-act-btn" onclick='App.setReply(${m.id},${q(m.user_name||'')})'>↩</button><button class="dc-act-btn ${saved?'active':''}" onclick="App.toggleSavedMessage(${m.id})" title="${saved?'Remove saved message':'Save message locally'}">SV</button><button class="dc-act-btn" onclick="App.showRP(${m.id})">😀</button>`;if(!isMe)a+=`<button class="dc-act-btn" onclick="App.reportMsg(${m.id})">⚑</button>`;if(isMe)a+=`<button class="dc-act-btn" onclick="App.editMsg(${m.id})">✏️</button>`;if(isMe||isMod)a+=`<button class="dc-act-btn" onclick="App.delMsg(${m.id})">🗑️</button>`;if(isMod)a+=`<button class="dc-act-btn" onclick="App.togglePin(${m.id})">📌</button>`;return a;},

  async sendMsg(){const input=document.getElementById('chat-input');if(!input)return;const text=input.value.trim();const hasUpload=!!this._pendingUpload;if((!text&&!hasUpload)||!this.ch)return;const s=this._session;
    if(!this._requireDb()){this._setComposerState(this._dbMsg(),'error');return;}
    if(this.ch==='announcements'&&!this.isStaff()){this._setComposerState('Only moderators and owners can post in announcements.','warn');return;}
    if(this.ch==='votes'&&!this.isStaff()){this._setComposerState('Only moderators can create votes here. You can still vote on polls.','warn');return;}
    if(this.ch==='votes'&&(hasUpload||!text.toLowerCase().startsWith('/poll '))){this._setComposerState('Votes channel only accepts polls. Use /poll Question | Option A | Option B','warn');return;}
    let outgoing='',restoreValue=text,rateBase=text;
    if(hasUpload){
      if(text){
        const captionGuard=this._messageGuard(text);
        if(!captionGuard.ok){this._setComposerState(captionGuard.msg,'error');return;}
      }
      rateBase=`[image] ${this._pendingUpload?.name||'upload'} ${text}`.trim();
      const spam=await this._canSendMessage(rateBase);
      if(!spam.ok){this._setComposerState(spam.msg,'error');return;}
      this._setComposerState('Uploading image...');
      const asset=await this._uploadImageAsset(this._pendingUpload);
      if(!asset?.ok||!asset?.src){
        this._setComposerState(asset?.error||'Image upload failed.','error');
        return;
      }
      outgoing=buildImageContent({src:asset.src,name:this._pendingUpload?.name||'image',caption:text,mime:this._pendingUpload?.mime||'',mode:asset.mode});
    }else{
      const commandResult=this._slashCommand(text);
      if(commandResult==='__unknown__'){this._setComposerState('Unknown command. Try /help','warn');return;}
      if(this.ch==='votes'&&commandResult?.type!=='poll'){this._setComposerState('Use /poll Question | Option A | Option B','warn');return;}
      outgoing=commandResult?.type==='poll'?buildPollContent(commandResult.question,commandResult.options):(commandResult||text);
      const guard=this._messageGuard(outgoing);
      if(!guard.ok){this._setComposerState(guard.msg,'error');return;}
      const spam=await this._canSendMessage(outgoing);
      if(!spam.ok){this._setComposerState(spam.msg,'error');return;}
    }
    input.value='';this._updateComposerMeta();this._setComposerState(hasUpload?'Sending image...':'Sending...');
    const{error}=await sb.from('chaty_messages').insert({channel_id:this.ch,user_id:s.id,user_name:this._displayName(this._me||{id:s.id,display_name:s.name},s.id),content:outgoing,platform:'chaty',reply_to:this.replyTo||null});
    if(error){input.value=restoreValue;this._setDraft(this.ch,restoreValue);this._updateComposerMeta();this._setComposerState(error.message,'error');return;}
    const now=Date.now();this._recentSends.push(now);this._trimSendWindows(now);this._lastSendAt=now;
    this._setComposerState(hasUpload?`Image sent • ${this._rateLimit} msgs / ${Math.round(this._windowMs/1000)}s limit`:`Sent • ${this._rateLimit} msgs / ${Math.round(this._windowMs/1000)}s limit`);
    this._clearDraft(this.ch);
    this.clearPendingUpload();
    this.cancelReply();sb.from('chaty_typing').delete().eq('user_id',s.id).then(()=>{});
    // Alyon Bridge is retired: new messages stay only in DIHCORD.
  },

  // Typing
  _onType(){if(!this._requireDb(false))return;const s=this._session;sb.from('chaty_typing').upsert({user_id:s.id,channel_id:this.ch,started_at:new Date().toISOString()}).then(()=>{});clearTimeout(this._typingTimer);this._typingTimer=setTimeout(()=>sb.from('chaty_typing').delete().eq('user_id',s.id).then(()=>{}),4000);},
  async _refreshTyping(force=false){if(!this._requireDb(false)||!this.ch||this.page!=='chat')return;const now=Date.now();if(!force&&now-this._lastTypingRefreshAt<this._typingPollMs-1000)return;this._lastTypingRefreshAt=now;const{data}=await sb.from('chaty_typing').select('user_id,started_at').eq('channel_id',this.ch);const s=this._session;const others=(data||[]).filter(t=>t.user_id!==s.id&&Date.now()-new Date(t.started_at).getTime()<8000);const el=document.getElementById('dc-typing');if(!el)return;if(!others.length){el.textContent='';return;}const names=others.map(t=>{const u=this._cache[t.user_id];return this._displayName(u||{id:t.user_id,display_name:t.user_id},t.user_id);});el.innerHTML=`<span class="dc-typing-dots">●●●</span> <strong>${names.join(', ')}</strong> ${names.length===1?'is':'are'} typing...`;},

  // Reactions
  showRP(id){document.querySelectorAll('.dc-react-picker').forEach(e=>e.remove());const el=document.querySelector(`[data-msg-id="${id}"]`);if(!el)return;const p=document.createElement('div');p.className='dc-react-picker';p.innerHTML=EMOJIS.map(e=>`<button class="dc-react-emoji" onclick='App.react(${id},${q(e)})'>${e}</button>`).join('');el.appendChild(p);setTimeout(()=>document.addEventListener('click',function rm(){p.remove();document.removeEventListener('click',rm);},{once:true}),10);},
  async react(id,emoji){if(!this._requireDb())return;document.querySelectorAll('.dc-react-picker').forEach(e=>e.remove());const{data:msg}=await sb.from('chaty_messages').select('reactions').eq('id',id).single();if(!msg)return;const r=msg.reactions||{};if(!r[emoji])r[emoji]=[];const i=r[emoji].indexOf(this._session.id);if(i===-1)r[emoji].push(this._session.id);else r[emoji].splice(i,1);if(r[emoji].length===0)delete r[emoji];await sb.from('chaty_messages').update({reactions:r}).eq('id',id);},
  async reportMsg(id){if(!this._requireDb())return;const reason=(prompt('Report reason: spam, unsafe link, harassment, other')||'').trim().slice(0,120);if(!reason)return;await sb.from('chaty_mod_log').insert({action:'REPORT_MESSAGE',target_id:String(id),mod_id:this._session.id,reason});alert('Report sent to staff.');},

  setReply(id,name){this.replyTo=id;const bar=document.getElementById('dc-reply-bar');bar.classList.remove('hidden');bar.innerHTML=`<span>Replying to <strong>${esc(name)}</strong></span><button class="dc-reply-cancel" onclick="App.cancelReply()">✕</button>`;document.getElementById('chat-input')?.focus();},
  cancelReply(){this.replyTo=null;document.getElementById('dc-reply-bar')?.classList.add('hidden');},
  async editMsg(id){if(!this._requireDb())return;const{data:m}=await sb.from('chaty_messages').select('content').eq('id',id).single();if(!m)return;const t=prompt('Edit:',m.content);if(t===null)return;const clean=t.trim();if(!clean)return;if(clean.length>this._maxMessageLength){alert(`Message is too long. Max ${this._maxMessageLength} characters.`);return;}await sb.from('chaty_messages').update({content:clean,edited:true}).eq('id',id);},
  async delMsg(id){if(!this._requireDb()||!confirm('Delete?'))return;await sb.from('chaty_messages').delete().eq('id',id);},
  async togglePin(id){if(!this._requireDb())return;const{data:m}=await sb.from('chaty_messages').select('pinned').eq('id',id).single();if(!m)return;await sb.from('chaty_messages').update({pinned:!m.pinned}).eq('id',id);},
  async showPins(){if(!this._requireDb())return;const{data:pins}=await sb.from('chaty_messages').select('id,user_id,user_name,content,created_at').eq('channel_id',this.ch).eq('pinned',true).order('created_at',{ascending:false}).limit(30);const ex=document.querySelector('.dc-pins-panel');if(ex){ex.remove();return;}const p=document.createElement('div');p.className='dc-pins-panel';p.innerHTML=`<div class="dc-pins-header">📌 Pinned<button class="dc-act-btn" onclick="this.closest('.dc-pins-panel').remove()" style="margin-left:auto">✕</button></div>${(pins||[]).length?(pins||[]).map(m=>`<div class="dc-pin-item"><strong>${esc(m.user_name||m.user_id||'user')}</strong>: ${esc(this._messagePreview(m,80))}</div>`).join(''):'<div style="padding:12px;color:var(--t3)">No pins</div>'}`;document.getElementById('chat-area').appendChild(p);},

  async _loadMembers(){if(!this._requireDb(false)||this.page!=='chat')return;const{data:users}=await sb.from('chaty_users').select('id,display_name,avatar_color,role,banned,muted,mute_reason,user_status,bio,warnings');await this._syncExpiredMutes(users||[]);const filtered=(users||[]).filter(u=>!this._memberFilter||`${this._displayName(u,u.id)} ${u.id}`.toLowerCase().includes(this._memberFilter));const p=document.getElementById('dc-members');if(!p)return;p.innerHTML=`<div class="dc-members-search"><input class="dc-filter" type="text" placeholder="Search member..." value="${attr(this._memberFilter)}" oninput="App.setMemberFilter(this.value)"></div><div class="dc-members-title">MEMBERS — ${filtered.length}</div>${filtered.map(u=>`<div class="dc-member" onclick='App.showProfile(${q(u.id)},${q('chaty')})'>${this._avatarHtml(u,u.avatar_color||'#5e8ed6','dc-member-av',u.id,u.banned?'opacity:.3':'')}<div class="dc-member-info"><span class="dc-member-name">${esc(this._displayName(u,u.id))}${u.banned?' 🚫':''}${u.muted?' 🔇':''}</span>${u.role&&u.role!=='user'?` <span class="dc-role-badge" style="background:${u.role==='owner'?'var(--gold)':'var(--green)'}">${u.role.toUpperCase()}</span>`:''}<div class="dc-member-role">${stDot(u.user_status||'online')} @${u.id}</div></div></div>`).join('')}`;},
  toggleMembers(){document.getElementById('dc-members')?.classList.toggle('hidden');},

  // Profile popup
  async showProfile(uid,plat){
    if(!this._requireDb())return;
    document.querySelectorAll('.pp-overlay,.profile-popup').forEach(e=>e.remove());
    let name=uid,color='#5e8ed6',role='user',bio='',banner='#14161e',status='online',warnings=0,muted=false,banned=false,muteReason='',banReason='',targetUser=null;
    if(plat==='alyon'){const cid=uid.replace('CHATY:','');const{data:c}=await sb.from('citizens').select('*').eq('citizen_id',cid).single();if(c){name=c.display_name||c.name;color=c.avatar_color||'#c9a84c';bio=c.bio||'';banner=c.banner_color||'#1a1c24';}else name=cid;}
    else{const{data:u}=await sb.from('chaty_users').select('*').eq('id',uid).single();if(u){targetUser=u;name=this._displayName(u,u.id);color=u.avatar_color;role=u.role||'user';bio=this._cleanBio(u);banner=u.banner_color||'#14161e';status=u.user_status||'online';warnings=Number(u.warnings)||0;muted=!!u.muted;banned=!!u.banned;muteReason=u.mute_reason||'';banReason=u.ban_reason||'';}}
    const activeWarnings=plat==='alyon'?[]:await this._getActiveWarnings(uid);
    const canSeeStanding=plat!=='alyon'&&(this.isStaff()||uid===this._session?.id);
    const canModerate=plat==='chaty'&&this.isStaff()&&uid!==this._session?.id&&role!=='owner';
    const standing=this._warningInfo({warnings,muted,banned,mute_reason:muteReason,ban_reason:banReason});
    const targetMeta=targetUser?userMeta(targetUser):{theme:'default',statusNote:''};
    const ov=document.createElement('div');ov.className='pp-overlay';const pp=document.createElement('div');pp.className=`profile-popup pf-theme-${cleanProfileTheme(targetMeta.theme||'default')}`;
    pp.innerHTML=`<div class="pp-banner" style="background:${banner}"></div><div class="pp-body"><button class="pp-close" onclick="this.closest('.profile-popup').remove();document.querySelector('.pp-overlay')?.remove()">✕</button>${plat==='alyon'?this._avatarShell(initial(name),color,'pp-avatar','none'):this._avatarHtml(targetUser||{display_name:name,id:uid},color,'pp-avatar',name)}<div class="pp-name">${stDot(status)} ${esc(name)}</div><div class="pp-id">@${esc(uid.replace('CHATY:',''))}</div>${targetMeta.statusNote?`<div class="pp-bio">${esc(targetMeta.statusNote)}</div>`:''}${role!=='user'?`<div style="margin-top:4px"><span class="role-tag role-${role}">${role}</span></div>`:''}<div style="margin-top:6px"><span class="dc-plat-badge ${plat==='alyon'?'plat-alyon':'plat-chaty'}">${plat==='alyon'?'Alyon':'Chaty'}</span></div>${bio?`<div class="pp-bio">${esc(bio)}</div>`:''}${canSeeStanding?`<div class="pp-section"><div class="pf-section-title">ACCOUNT STANDING</div><div class="pp-mini"><span>State</span>${this._warningChip({warnings,muted,banned,mute_reason:muteReason,ban_reason:banReason})}</div><div class="pp-mini"><span>Warnings</span><strong>${standing.count}</strong></div><div class="pp-bio">${esc(standing.detail)}</div><div class="pf-warning-list">${this._renderWarningReasons(activeWarnings)}</div></div>`:''}${canModerate?`<div class="pp-section"><div class="pf-section-title">MOD PANEL</div><div class="pp-actions"><button class="btn btn-outline" onclick='App.warnUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Warn</button><button class="btn btn-outline" onclick='App.unwarnUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Unwarn</button><button class="btn btn-outline" onclick='App.tempMuteUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Temp Mute</button><button class="btn btn-outline" onclick='App.unmuteUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Unmute</button><button class="btn btn-outline" onclick='App.banUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Ban</button><button class="btn btn-outline" onclick='App.startDm(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>DM</button></div></div>`:''}</div>`;
    ov.onclick=()=>{ov.remove();pp.remove();};document.body.appendChild(ov);document.body.appendChild(pp);
  },

  // DM
  async startDm(tid){if(!this._requireDb())return;const s=this._session;const dmId='dm_'+[s.id,tid].sort().join('_');const meName=this._displayName(this._me||{id:s.id,display_name:s.name},s.id);const target=this._cache[tid];const targetName=this._displayName(target||{id:tid,display_name:tid},tid);const{data:ex}=await sb.from('chaty_channels').select('*').eq('id',dmId).single();if(!ex)await sb.from('chaty_channels').insert({id:dmId,name:meName+' & '+targetName,type:'dm',category:'DMs',members:[s.id,tid],created_by:s.id,position:99});await this.loadChs();this.openChat(dmId);},
  focusVotePollMaker(){
    if(this.ch!=='votes'){this.openChat('votes');setTimeout(()=>document.getElementById('vote-q')?.focus(),250);return;}
    document.getElementById('vote-q')?.focus();
    document.getElementById('vote-poll-maker')?.scrollIntoView({behavior:'smooth',block:'center'});
  },
  fillVotePollExample(){
    const q=document.getElementById('vote-q'),o1=document.getElementById('vote-o1'),o2=document.getElementById('vote-o2'),o3=document.getElementById('vote-o3'),o4=document.getElementById('vote-o4');
    if(q)q.value='What should we do next?';
    if(o1)o1.value='Event';
    if(o2)o2.value='Game night';
    if(o3)o3.value='New channel';
    if(o4)o4.value='';
    q?.focus();
  },
  async createVotePollSimple(){
    if(!this._requireDb()||!this.isStaff())return;
    const msg=document.getElementById('vote-poll-msg');
    const question=(document.getElementById('vote-q')?.value||'').trim().slice(0,120);
    const options=['vote-o1','vote-o2','vote-o3','vote-o4'].map(id=>(document.getElementById(id)?.value||'').trim().slice(0,40)).filter(Boolean);
    const setMsg=(text,tone='')=>{if(msg){msg.textContent=text;msg.className='admin-msg '+(tone||'');}else this._setComposerState(text,tone==='error'?'error':tone==='warn'?'warn':'');};
    if(this.ch!=='votes'){setMsg('Open #votes to create polls here.','warn');return;}
    if(!question){setMsg('Question is required.','error');return;}
    if(options.length<2){setMsg('Add at least 2 options.','error');return;}
    const guard=this._messageGuard(`${question} ${options.join(' ')}`);
    if(!guard.ok){setMsg(guard.msg,'error');return;}
    const spam=await this._canSendMessage(`poll ${question} ${options.join(' ')}`);
    if(!spam.ok){setMsg(spam.msg,'error');return;}
    const s=this._session;
    const content=buildPollContent(question,options);
    const {error}=await sb.from('chaty_messages').insert({channel_id:'votes',user_id:s.id,user_name:this._displayName(this._me||{id:s.id,display_name:s.name},s.id),content,platform:'chaty'});
    if(error){setMsg(error.message,'error');return;}
    const now=Date.now();this._recentSends.push(now);this._trimSendWindows(now);this._lastSendAt=now;
    ['vote-q','vote-o1','vote-o2','vote-o3','vote-o4'].forEach(id=>{const el=document.getElementById(id);if(el)el.value='';});
    setMsg('Poll posted in #votes.','success');
  },
  showNewCh(){const area=document.getElementById('chat-area');const ex=area.querySelector('.form-block');if(ex){ex.remove();return;}const f=document.createElement('div');f.className='form-block';f.innerHTML=`<div class="form-title">Create Channel</div><div class="form-grid"><div><label class="form-label">Name</label><input type="text" id="nc-n" class="form-input"></div><div><label class="form-label">Description</label><input type="text" id="nc-d" class="form-input"></div></div><button class="btn btn-accent" onclick="App.createCh()" style="margin-top:12px">Create</button>`;area.appendChild(f);},
  async createCh(){if(!this._requireDb())return;const n=document.getElementById('nc-n').value.trim();if(!n)return;const cleanName=n.slice(0,this._maxChannelNameLength);const slug=cleanName.toLowerCase().replace(/[^a-z0-9]+/g,'-').replace(/^-+|-+$/g,'');if(slug.length<2){alert('Use at least 2 letters or numbers in the channel name.');return;}const id='chaty-'+slug;const desc=document.getElementById('nc-d').value.trim().slice(0,this._maxChannelDescLength);const{data:last}=await sb.from('chaty_channels').select('position').eq('type','public').order('position',{ascending:false}).limit(1);const position=(last?.[0]?.position||0)+1;const{error}=await sb.from('chaty_channels').insert({id,name:'# '+cleanName,description:desc,type:'public',category:'CHANNELS',created_by:this._session.id,position});if(error){alert(error.message);return;}document.querySelector('.form-block')?.remove();await this.loadChs();this.openChat(id);},

  /* ===== PROFILE PAGE ===== */
  async goProfile(){
    if(!this._requireDb())return;
    this.page='profile';this.ch=null;if(this._sub&&sbReady()){sb.removeChannel(this._sub);this._sub=null;}if(this._tsub&&sbReady()){sb.removeChannel(this._tsub);this._tsub=null;}document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));document.getElementById('nav-profile')?.classList.add('dc-active');document.getElementById('dc-members')?.classList.add('hidden');
    if(this._sub&&sbReady()){sb.removeChannel(this._sub);this._sub=null;}
    const{data:me}=await sb.from('chaty_users').select('*').eq('id',this._session.id).single();if(!me)return;this._me=me;
    const meta=userMeta(me);
    const activeWarnings=await this._getActiveWarnings(this._session.id);
    const standing=this._warningInfo(me);
    const area=document.getElementById('chat-area');
    area.innerHTML=`<div style="padding:24px 32px;overflow-y:auto;flex:1">
      <div class="pf-card pf-theme-${cleanProfileTheme(meta.theme||'default')}"><div class="pf-banner" style="background:${me.banner_color||'#14161e'}"></div><div class="pf-card-body">${this._avatarHtml(me,me.avatar_color,'pf-avatar',me.id)}<div class="pf-display-name">${stDot(me.user_status)} ${esc(this._displayName(me,me.id))}</div><div class="pf-username">@${me.id}</div>${meta.statusNote?`<div class="pp-bio">${esc(meta.statusNote)}</div>`:''}${me.role&&me.role!=='user'?`<div style="margin-top:4px"><span class="role-tag role-${me.role}">${me.role}</span></div>`:''}<div class="pf-divider"></div>${this._cleanBio(me)?`<div class="pf-section"><div class="pf-section-title">ABOUT ME</div><div class="pf-bio">${esc(this._cleanBio(me))}</div></div>`:''}<div class="pf-section"><div class="pf-section-title">ACCOUNT STANDING</div><div class="pf-warning-box"><div class="pf-warning-row"><span>Status</span>${this._warningChip(me)}</div><div class="pf-warning-row"><span>Warnings</span><strong>${standing.count}</strong></div><div class="pf-warning-note">${esc(standing.detail)}</div><div class="pf-warning-list">${this._renderWarningReasons(activeWarnings)}</div></div></div><div class="pf-section"><div class="pf-section-title">YOUR PREFIX</div><div class="pf-field">${meta.prefix?esc(meta.prefix):'No prefix yet'}</div></div><div class="pf-section"><div class="pf-section-title">Avatar Style</div><div class="pf-field">${esc(this._avatarDecorLabel(meta.decor||'none'))} / ${esc(this._avatarFrameLabel(meta.frame||'none'))}</div></div><div class="pf-section"><div class="pf-section-title">Profile Theme</div><div class="pf-field">${esc(this._profileThemeLabel(meta.theme||'default'))}</div></div><div class="pf-section"><div class="pf-section-title">JOINED</div><div class="pf-field">${new Date(me.created_at).toLocaleDateString()}</div></div>
        <button class="btn btn-accent pf-edit-btn" onclick="App.showEditProfile()">Edit Profile</button></div></div>
      <div id="edit-pf" class="hidden"></div>
    </div>`;
  },

  async showEditProfile(){const me=this._me;const f=document.getElementById('edit-pf');f.classList.toggle('hidden');if(!f.classList.contains('hidden')){
    const meta=userMeta(me);
    const decorOptions=this._avatarDecorOptions().map(item=>`<option value="${item.value}" ${cleanAvatarDecor(meta.decor||'none')===item.value?'selected':''}>${esc(item.label)}</option>`).join('');
    const frameOptions=this._avatarFrameOptions().map(item=>`<option value="${item.value}" ${cleanAvatarFrame(meta.frame||'none')===item.value?'selected':''}>${esc(item.label)}</option>`).join('');
    const themeOptions=this._profileThemeOptions().map(item=>`<option value="${item.value}" ${cleanProfileTheme(meta.theme||'default')===item.value?'selected':''}>${esc(item.label)}</option>`).join('');
    f.innerHTML=`<div class="pf-edit-card"><div class="form-title">Edit Profile</div><div class="pf-edit-banner" id="ep-bp" style="background:${me.banner_color||'#14161e'}"></div><div class="form-grid" style="margin-top:16px">
      <div><label class="form-label">Display Name</label><input type="text" id="ep-dn" class="form-input" value="${me.display_name||''}"></div>
      <div><label class="form-label">Status</label><select id="ep-st" class="form-input"><option value="online" ${me.user_status==='online'?'selected':''}>🟢 Online</option><option value="idle" ${me.user_status==='idle'?'selected':''}>🌙 Idle</option><option value="dnd" ${me.user_status==='dnd'?'selected':''}>⛔ DND</option><option value="invisible" ${me.user_status==='invisible'?'selected':''}>⚫ Invisible</option></select></div>
      <div><label class="form-label">Prefix</label><input type="text" id="ep-prefix" class="form-input" maxlength="${this._maxPrefixLength}" value="${attr(meta.prefix)}" placeholder="VIP"></div>
      <div><label class="form-label">Status Note</label><input type="text" id="ep-note" class="form-input" maxlength="64" value="${attr(meta.statusNote||'')}" placeholder="studying, gaming, online"></div>
      <div><label class="form-label">Avatar Emoji</label><input type="text" id="ep-avatar" class="form-input" maxlength="4" value="${attr(meta.avatar)}" placeholder="😀"></div>
      <div><label class="form-label">Avatar Decor</label><select id="ep-decor" class="form-input">${decorOptions}</select></div>
      <div><label class="form-label">Avatar Frame</label><select id="ep-frame" class="form-input">${frameOptions}</select></div>
      <div><label class="form-label">Profile Theme</label><select id="ep-theme" class="form-input">${themeOptions}</select></div>
      <div><label class="form-label">Avatar Photo</label><input type="file" id="ep-avatar-file" class="form-input" accept="image/png,image/jpeg,image/webp" onchange="App.handleProfileAvatarPick(this)"><input type="hidden" id="ep-avatar-img" value="${attr(meta.avatarImg||'')}"><input type="hidden" id="ep-avatar-img-preview" value=""><div id="ep-upload-msg" class="mono" style="margin-top:6px;color:var(--t3)">${meta.avatarImg?'Photo avatar active. Pick a new file to replace it.':'Optional PNG/JPG/WEBP photo avatar.'}</div><button type="button" class="btn btn-outline" style="margin-top:8px" onclick="document.getElementById('ep-avatar-img').value='';document.getElementById('ep-avatar-img-preview').value='';document.getElementById('ep-avatar-file').value='';document.getElementById('ep-upload-msg').textContent='Photo avatar removed. Save to apply.';App._updateDecorPreview()">Remove Photo</button></div>
      <div><label class="form-label">Banner Color</label><div class="pf-color-row"><input type="color" id="ep-bc" class="pf-color-input" value="${me.banner_color||'#14161e'}"><div class="pf-color-presets">${['#c0392b','#e67e22','#f1c40f','#27ae60','#2c6fbb','#9b59b6','#14161e','#c9a84c'].map(x=>`<div class="pf-color-swatch" style="background:${x}" onclick="document.getElementById('ep-bc').value='${x}';document.getElementById('ep-bp').style.background='${x}'"></div>`).join('')}</div></div></div>
    </div><div id="ep-avatar-preview" class="pf-avatar-preview"></div><label class="form-label" style="margin-top:12px">About Me</label><textarea id="ep-bio" class="form-input form-textarea">${this._cleanBio(me)||''}</textarea>
    <div style="display:flex;gap:8px;margin-top:14px"><button class="btn btn-accent" onclick="App.saveProfile()">Save</button><button class="btn btn-outline" onclick="document.getElementById('edit-pf').classList.add('hidden')">Cancel</button></div></div>`;
    document.getElementById('ep-bc').addEventListener('input',e=>document.getElementById('ep-bp').style.background=e.target.value);
    document.getElementById('ep-avatar')?.addEventListener('input',()=>this._updateDecorPreview());
    document.getElementById('ep-dn')?.addEventListener('input',()=>this._updateDecorPreview());
    document.getElementById('ep-decor')?.addEventListener('change',()=>this._updateDecorPreview());
    document.getElementById('ep-frame')?.addEventListener('change',()=>this._updateDecorPreview());
    document.getElementById('ep-theme')?.addEventListener('change',()=>this._updateDecorPreview());
    document.getElementById('ep-bc')?.addEventListener('input',()=>this._updateDecorPreview());
    this._updateDecorPreview();
  }},

  async saveProfile(){if(!this._requireDb())return;const displayName=(document.getElementById('ep-dn').value.trim()||this._session.id).slice(0,this._maxNameLength);const prefix=(document.getElementById('ep-prefix').value.trim()||'').replace(/[^\w-]/g,'').slice(0,this._maxPrefixLength);const avatar=(document.getElementById('ep-avatar').value.trim()||'').slice(0,4);const decor=cleanAvatarDecor(document.getElementById('ep-decor').value||'none');const frame=cleanAvatarFrame(document.getElementById('ep-frame')?.value||'none');const theme=cleanProfileTheme(document.getElementById('ep-theme')?.value||'default');const statusNote=(document.getElementById('ep-note')?.value||'').trim().slice(0,64);const bio=document.getElementById('ep-bio').value.trim().slice(0,this._maxBioLength);let avatarImg=(document.getElementById('ep-avatar-img')?.value||'').trim();const file=document.getElementById('ep-avatar-file')?.files?.[0];const uploadMsg=document.getElementById('ep-upload-msg');if(file){if(uploadMsg)uploadMsg.textContent='Uploading avatar photo...';const uploaded=await this._uploadProfileAvatarAsset(file);if(!uploaded.ok){if(uploadMsg)uploadMsg.textContent=uploaded.error;alert(uploaded.error);return;}avatarImg=uploaded.src;}await sb.from('chaty_users').update({display_name:displayName,user_status:document.getElementById('ep-st').value,banner_color:document.getElementById('ep-bc').value,bio:buildUserBio(bio,{prefix,avatar,decor,avatarImg,frame,theme,statusNote})}).eq('id',this._session.id);this._session.name=displayName;localStorage.setItem('chaty_session',JSON.stringify(this._session));this.goProfile();},

  /* ===== ADMIN ===== */
  _adminUserCard(u){return`<div class="admin-user"><div class="admin-user-main"><div class="admin-user-line"><span class="admin-user-name">${esc(this._displayName(u,u.id))}</span><span class="mono">@${esc(u.id)}</span>${u.role&&u.role!=='user'?`<span class="role-tag role-${u.role}">${u.role}</span>`:''}${u.banned?'<span class="status-tag st-banned">BANNED</span>':u.muted?'<span class="status-tag st-muted">MUTED</span>':'<span class="st-ok">OK</span>'}</div><div class="admin-user-meta">Warnings: ${u.warnings||0}${u.muted&&u.mute_reason?` • ${esc(this._muteLabel(u.mute_reason))}`:''}</div></div><div class="actions-cell">${u.role==='owner'?'<span class="mono" style="color:var(--gold)">OWNER</span>':`${u.role!=='mod'?`<button class="btn-sm btn-mod" onclick='App.setRole(${q(u.id)},"mod")'>Mod</button>`:`<button class="btn-sm btn-edit" onclick='App.setRole(${q(u.id)},"user")'>Unmod</button>`}<button class="btn-sm btn-warn" onclick='App.warnUser(${q(u.id)})'>Warn</button><button class="btn-sm btn-edit" onclick='App.unwarnUser(${q(u.id)})'>Unwarn</button>${u.muted?`<button class="btn-sm btn-edit" onclick='App.unmuteUser(${q(u.id)})'>Unmute</button>`:`<button class="btn-sm btn-mute" onclick='App.tempMuteUser(${q(u.id)})'>TempMute</button>`}${u.banned?`<button class="btn-sm btn-mod" onclick='App.unbanUser(${q(u.id)})'>Unban</button>`:`<button class="btn-sm btn-ban" onclick='App.banUser(${q(u.id)})'>Ban</button>`}<button class="btn-sm btn-del" onclick='App.delUser(${q(u.id)})'>Delete</button><button class="btn-sm btn-edit" onclick='App.showProfile(${q(u.id)},"chaty")'>Profile</button>`}</div></div>`;},
  _adminChannelCard(c){return`<div class="admin-mini-item"><div><div style="font-weight:700">${esc(c.name)}</div><div class="mono">${esc(c.id)}</div></div><button class="btn-sm btn-del" onclick='App.delChannel(${q(c.id)})'>Delete</button></div>`;},
  _adminLogCard(l){return`<div class="admin-log-item"><div class="admin-log-top"><div class="admin-log-title">${esc(l.action)}</div><div class="mono">${new Date(l.created_at).toLocaleString()}</div></div><div class="admin-log-meta">Target: ${esc(l.target_id)} • By: ${esc(l.mod_id)}</div>${l.reason?`<div style="margin-top:6px;color:var(--t2)">${esc(l.reason)}</div>`:''}</div>`;},
  async goAdmin(){
    if(!this._requireDb()||!this.isStaff())return;this._adminRefreshing=true;this.page='admin';this.ch=null;if(this._sub&&sbReady()){sb.removeChannel(this._sub);this._sub=null;}if(this._tsub&&sbReady()){sb.removeChannel(this._tsub);this._tsub=null;}document.getElementById('dc-members')?.classList.add('hidden');
    document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));document.getElementById('nav-admin')?.classList.add('dc-active');
    if(this._sub&&sbReady()){sb.removeChannel(this._sub);this._sub=null;}
    const area=document.getElementById('chat-area');
    area.innerHTML=`<div class="admin-panel"><h2 style="font-size:22px;font-weight:700;margin-bottom:20px;font-family:var(--display)">⚙️ Admin Panel</h2><div class="form-block"><div class="mono" style="color:var(--t2)">Loading admin data...</div></div></div>`;
    const results=await Promise.allSettled([
      withTimeout(sb.from('chaty_users').select('id,display_name,role,banned,muted,mute_reason,warnings,bio').order('id'),8000,'Loading admin users'),
      withTimeout(sb.from('chaty_channels').select('id,name,type,position').order('position'),8000,'Loading admin channels'),
      withTimeout(sb.from('chaty_mod_log').select('action,target_id,mod_id,reason,created_at').order('created_at',{ascending:false}).limit(20),8000,'Loading moderation log')
    ]);
    const usersRes=results[0].status==='fulfilled'?results[0].value:{data:[],error:{message:results[0].reason?.message||'Failed to load users'}};
    const channelsRes=results[1].status==='fulfilled'?results[1].value:{data:[],error:{message:results[1].reason?.message||'Failed to load channels'}};
    const logsRes=results[2].status==='fulfilled'?results[2].value:{data:[],error:{message:results[2].reason?.message||'Failed to load mod log'}};
    const users=usersRes.data||[];
    const channels=channelsRes.data||[];
    const logs=logsRes.data||[];
    const errs=[usersRes.error,channelsRes.error,logsRes.error].filter(Boolean).map(e=>e.message);
    const staffCount=users.filter(u=>u.role==='owner'||u.role==='mod').length,bannedCount=users.filter(u=>u.banned).length,mutedCount=users.filter(u=>u.muted).length;
    area.innerHTML=`<div class="admin-panel"><div class="admin-shell">
      <div class="admin-topbar"><div><h2 style="font-size:24px;font-weight:800;font-family:var(--display)">Server Admin</h2><div class="mono" style="color:var(--t3);margin-top:6px">Discord-style dashboard with anti-spam aware moderation tools.</div></div><button class="btn btn-outline" onclick="App.goAdmin()">Refresh</button></div>
      ${errs.length?`<div class="admin-msg error">${esc(errs.join(' | '))}</div>`:''}
      <div class="admin-overview">
        <div class="admin-stat"><div class="admin-stat-label">Users</div><div class="admin-stat-value">${users.length}</div></div>
        <div class="admin-stat"><div class="admin-stat-label">Staff</div><div class="admin-stat-value">${staffCount}</div></div>
        <div class="admin-stat"><div class="admin-stat-label">Muted</div><div class="admin-stat-value">${mutedCount}</div></div>
        <div class="admin-stat"><div class="admin-stat-label">Banned</div><div class="admin-stat-value">${bannedCount}</div></div>
      </div>
      <div class="admin-grid">
        <div class="admin-stack">
          <div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Users</div><div class="admin-card-sub">Showing all ${users.length} users</div></div></div><div class="admin-list">${users.map(u=>this._adminUserCard(u)).join('')||'<div style="color:var(--t3)">No users found</div>'}</div></div>
          <div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Channels</div><div class="admin-card-sub">Fast channel controls</div></div></div><div class="admin-mini-list">${channels.map(c=>this._adminChannelCard(c)).join('')||'<div style="color:var(--t3)">No channels found</div>'}</div></div>
        </div>
        <div class="admin-stack">
          <div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Mod Log</div><div class="admin-card-sub">Latest ${logs.length} actions</div></div></div><div class="admin-mini-list">${logs.map(l=>this._adminLogCard(l)).join('')||'<div style="color:var(--t3)">No actions yet</div>'}</div></div>
          ${this.isPrimaryOwner()?this._homeNewsCardHtml():''}
          ${this.isPrimaryOwner()?this._siteLockCardHtml():''}
          <div class="admin-card"><div class="admin-card-head"><div><div class="admin-card-title">Quick Tools</div><div class="admin-card-sub">Purge and create accounts</div></div></div><button class="btn btn-red" onclick="App.purge()">Purge Channel</button><div id="purge-f" class="hidden form-block" style="margin-top:12px"></div><div class="form-block" style="margin-top:16px"><div class="form-title">Create User</div><div class="form-grid"><div><label class="form-label">Username</label><input type="text" id="au-id" class="form-input"></div><div><label class="form-label">Password</label><input type="text" id="au-pw" class="form-input"></div><div><label class="form-label">Role</label><select id="au-role" class="form-input"><option>user</option><option>mod</option></select></div></div><button class="btn btn-accent" onclick="App.createUser()" style="margin-top:12px">Create</button><div id="admin-msg" class="admin-msg"></div></div></div>
        </div>
      </div>
    </div></div>`;
    this._adminRefreshing=false;
    return;
  },

  // Mod actions
  async warnUser(uid){if(!this._requireDb())return;const reason=prompt('Warning reason:');if(!reason)return;const{data:u}=await sb.from('chaty_users').select('warnings').eq('id',uid).single();await sb.from('chaty_users').update({warnings:(u?.warnings||0)+1}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'WARN',target_id:uid,mod_id:this._session.id,reason});alert('Warning issued (total: '+((u?.warnings||0)+1)+')');this.goAdmin();},
  async unwarnUser(uid){if(!this._requireDb())return;const note=prompt('Reason for removing a warning:')||'Warning removed by moderator';const{data:u}=await sb.from('chaty_users').select('warnings').eq('id',uid).single();const next=Math.max(0,(Number(u?.warnings)||0)-1);await sb.from('chaty_users').update({warnings:next}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'UNWARN',target_id:uid,mod_id:this._session.id,reason:note.slice(0,120)});alert('Warning removed. Total warnings: '+next);this.goAdmin();},
  async muteUser(uid){if(!this._requireDb())return;const reason=prompt('Mute reason:');if(reason===null)return;await sb.from('chaty_users').update({muted:true,mute_reason:buildMuteReason((reason||'').slice(0,120))||null}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'MUTE',target_id:uid,mod_id:this._session.id,reason:(reason||'').slice(0,120)||null});alert('Muted');this.goAdmin();},
  async tempMuteUser(uid){if(!this._requireDb())return;const minutes=Math.max(1,Math.min(10080,Number(prompt('Mute for how many minutes?','60'))||0));if(!minutes)return;const reason=prompt('Temp mute reason:')||'Temporary mute';const until=new Date(Date.now()+minutes*60000).toISOString();await sb.from('chaty_users').update({muted:true,mute_reason:buildMuteReason(reason,until)}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'TEMP_MUTE',target_id:uid,mod_id:this._session.id,reason:`${reason} (until ${until})`});alert('Temporary mute set for '+minutes+' minutes.');this.goAdmin();},
  async unmuteUser(uid){if(!this._requireDb())return;await sb.from('chaty_users').update({muted:false,mute_reason:null}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'UNMUTE',target_id:uid,mod_id:this._session.id});this.goAdmin();},
  async banUser(uid){if(!this._requireDb())return;const reason=prompt('Ban reason:');if(reason===null)return;await sb.from('chaty_users').update({banned:true,ban_reason:(reason||'').slice(0,120)||null}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'BAN',target_id:uid,mod_id:this._session.id,reason:(reason||'').slice(0,120)||null});alert('Banned');this.goAdmin();},
  async unbanUser(uid){if(!this._requireDb())return;await sb.from('chaty_users').update({banned:false,ban_reason:null}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'UNBAN',target_id:uid,mod_id:this._session.id});this.goAdmin();},
  async setRole(uid,role){if(!this._requireDb()||!confirm('Set '+uid+' as '+role+'?'))return;await sb.from('chaty_users').update({role}).eq('id',uid);await sb.from('chaty_mod_log').insert({action:'ROLE_'+role.toUpperCase(),target_id:uid,mod_id:this._session.id});this.goAdmin();},
  async delUser(uid){if(!this._requireDb()||!confirm('DELETE '+uid+'?'))return;await sb.from('chaty_users').delete().eq('id',uid);await sb.from('chaty_mod_log').insert({action:'DELETE_USER',target_id:uid,mod_id:this._session.id});this.goAdmin();},
  async delChannel(cid){if(!this._requireDb()||!confirm('Delete #'+cid+'?'))return;await sb.from('chaty_channels').delete().eq('id',cid);await this.loadChs();this.goAdmin();},
  purge(){const f=document.getElementById('purge-f');f.classList.toggle('hidden');if(!f.classList.contains('hidden'))f.innerHTML=`<label class="form-label">Channel ID</label><input type="text" id="purge-id" class="form-input"><button class="btn btn-red" onclick="App.doPurge()" style="margin-top:8px">PURGE</button>`;},
  async doPurge(){if(!this._requireDb())return;const id=document.getElementById('purge-id').value.trim();if(!id||!confirm('DELETE ALL in '+id+'?'))return;await sb.from('chaty_messages').delete().eq('channel_id',id);await sb.from('chaty_mod_log').insert({action:'PURGE',target_id:id,mod_id:this._session.id});alert('Purged!');},
  async createUser(){if(!this._requireDb())return;const id=document.getElementById('au-id').value.trim().toLowerCase(),pw=document.getElementById('au-pw').value,role=document.getElementById('au-role').value,msg=document.getElementById('admin-msg');if(!id||!pw){msg.textContent='Fill fields';msg.className='admin-msg error';return;}if(!/^[a-z0-9_-]{3,24}$/.test(id)){msg.textContent='Use 3-24 letters, numbers, _ or -';msg.className='admin-msg error';return;}if(pw.length<4||pw.length>this._maxPasswordLength){msg.textContent='Password must be 4-'+this._maxPasswordLength+' chars';msg.className='admin-msg error';return;}const{data:ex}=await sb.from('chaty_users').select('id').eq('id',id).single();if(ex){msg.textContent='Taken';msg.className='admin-msg error';return;}const{error}=await sb.from('chaty_users').insert({id,password:pw,display_name:id,avatar_color:randColor(),role});if(error){msg.textContent=error.message;msg.className='admin-msg error';}else{msg.textContent='Created '+id;msg.className='admin-msg success';this.goAdmin();}},

  _snd(){if(this._settings.sounds===false)return;try{if(!this._audioCtx)this._audioCtx=new(window.AudioContext||window.webkitAudioContext)();const c=this._audioCtx,o=c.createOscillator(),g=c.createGain();o.connect(g);g.connect(c.destination);o.frequency.setValueAtTime(660,c.currentTime);o.frequency.setValueAtTime(880,c.currentTime+.08);g.gain.setValueAtTime(.2,c.currentTime);g.gain.exponentialRampToValueAtTime(.01,c.currentTime+.25);o.start(c.currentTime);o.stop(c.currentTime+.25);}catch(e){}}
};

window.App=App;

document.addEventListener('keydown',e=>{if(e.key==='Enter'&&!document.getElementById('auth-screen').classList.contains('hidden'))App.handleAuth();});
document.addEventListener('DOMContentLoaded',()=>App.init());
setInterval(()=>{if(App.page==='chat'&&App.ch)App._refreshTyping();},8000);
</script>
<script id="dih-runtime-guard-script">
App._warningInfo=App._warningInfo||function(user){
  const warnings=Math.max(0,Number(user?.warnings)||0);
  if(user?.banned)return{tone:'warn-bad',title:'BANNED',detail:user?.ban_reason||'Your access is blocked right now.',count:warnings};
  if(user?.muted)return{tone:'warn-warn',title:'MUTED',detail:this._muteLabel(user?.mute_reason)||'You can read, but you cannot send messages right now.',count:warnings};
  if(warnings>=3)return{tone:'warn-bad',title:`${warnings} WARNINGS`,detail:'Your account is close to bigger moderation action. Keep it clean.',count:warnings};
  if(warnings>0)return{tone:'warn-warn',title:`${warnings} WARNING${warnings===1?'':'S'}`,detail:'Warnings are now visible to you here. Slow down and follow the server rules.',count:warnings};
  return{tone:'warn-good',title:'CLEAN',detail:'No active warnings on your account.',count:0};
};
App._warningChip=App._warningChip||function(user){
  const info=this._warningInfo(user);
  return `<span class="warn-chip ${info.tone}">${esc(info.title)}</span>`;
};
App._renderUserPanel=function(user){
  const s=this._session||{};
  const current=user||this._me||{};
  const color=current.avatar_color||s.color||'#5e8ed6';
  const panel=document.getElementById('ch-user');
  if(!panel)return;
  const adminBtn=this.isStaff()?'<button class="dc-theme-btn" onclick="App.goAdmin()" title="Admin Panel">ADM</button>':'';
  panel.innerHTML=`${this._avatarHtml(current,color,'dc-user-av',s.id)}<div class="dc-user-info"><div class="dc-user-nm">${esc(this._displayName(current,s.id||'user'))}</div><div class="dc-user-id">@${esc(s.id||current.id||'')}</div><div class="dc-user-standing">${this._warningChip(current)}</div></div><div class="dc-user-actions"><button class="dc-theme-btn" onclick="App.toggleTheme()">${this._theme==='light'?'🌙':'☀️'}</button>${adminBtn}<button class="dc-logout" onclick="App.logout()">⏻</button></div>`;
};
const _showAppWarnings=App.showApp.bind(App);
App.showApp=async function(){
  await _showAppWarnings();
  this._syncNavShell();
  if(this._me)this._renderUserPanel(this._me);
};
App.goHome=async function(){
  this.page='home';this.ch=null;this.replyTo=null;this._closeLiveSubs();
  document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
  document.getElementById('nav-home')?.classList.add('dc-active');
  document.getElementById('dc-members')?.classList.add('hidden');
  if(this._me)this._renderUserPanel(this._me);
  const activeWarnings=this._session?.id?await this._getActiveWarnings(this._session.id):[];
  document.getElementById('chat-area').innerHTML=this._homeHtml(activeWarnings);
};
App.goProfile=async function(){
  if(!this._requireDb())return;
  this.page='profile';this.ch=null;this._closeLiveSubs();
  document.querySelectorAll('.dc-ch-item,.dc-nav-item').forEach(el=>el.classList.remove('dc-active'));
  document.getElementById('nav-profile')?.classList.add('dc-active');
  document.getElementById('dc-members')?.classList.add('hidden');
  const{data:me}=await sb.from('chaty_users').select('*').eq('id',this._session.id).single();
  if(!me)return;
  this._me=me;
  this._renderUserPanel(me);
  const standing=this._warningInfo(me);
  const activeWarnings=await this._getActiveWarnings(this._session.id);
  const meta=userMeta(me);
  const area=document.getElementById('chat-area');
  area.innerHTML=`<div style="padding:24px 32px;overflow-y:auto;flex:1"><div class="pf-card pf-theme-${cleanProfileTheme(meta.theme||'default')}"><div class="pf-banner" style="background:${me.banner_color||'#14161e'}"></div><div class="pf-card-body">${this._avatarHtml(me,me.avatar_color,'pf-avatar',me.id)}<div class="pf-display-name">${stDot(me.user_status)} ${esc(this._displayName(me,me.id))}</div><div class="pf-username">@${me.id}</div>${meta.statusNote?`<div class="pp-bio">${esc(meta.statusNote)}</div>`:''}${me.role&&me.role!=='user'?`<div style="margin-top:4px"><span class="role-tag role-${me.role}">${me.role}</span></div>`:''}<div class="pf-divider"></div>${this._cleanBio(me)?`<div class="pf-section"><div class="pf-section-title">ABOUT ME</div><div class="pf-bio">${esc(this._cleanBio(me))}</div></div>`:''}<div class="pf-section"><div class="pf-section-title">ACCOUNT STANDING</div><div class="pf-warning-box"><div class="pf-warning-row"><span>Status</span>${this._warningChip(me)}</div><div class="pf-warning-row"><span>Warnings</span><strong>${standing.count}</strong></div><div class="pf-warning-note">${esc(standing.detail)}</div><div class="pf-warning-list">${this._renderWarningReasons(activeWarnings)}</div></div></div><div class="pf-section"><div class="pf-section-title">YOUR PREFIX</div><div class="pf-field">${meta.prefix?esc(meta.prefix):'No prefix yet'}</div></div><div class="pf-section"><div class="pf-section-title">Avatar Style</div><div class="pf-field">${esc(this._avatarDecorLabel(meta.decor||'none'))} / ${esc(this._avatarFrameLabel(meta.frame||'none'))}</div></div><div class="pf-section"><div class="pf-section-title">Profile Theme</div><div class="pf-field">${esc(this._profileThemeLabel(meta.theme||'default'))}</div></div><div class="pf-section"><div class="pf-section-title">JOINED</div><div class="pf-field">${new Date(me.created_at).toLocaleDateString()}</div></div><button class="btn btn-accent pf-edit-btn" onclick="App.showEditProfile()">Edit Profile</button></div></div><div id="edit-pf" class="hidden"></div></div>`;
};
App.showProfile=async function(uid,plat){
  if(!this._requireDb())return;
  document.querySelectorAll('.pp-overlay,.profile-popup').forEach(e=>e.remove());
  let name=uid,color='#5e8ed6',role='user',bio='',banner='#14161e',status='online',warnings=0,muted=false,banned=false,muteReason='',banReason='',targetUser=null;
  if(plat==='alyon'){
    const cid=uid.replace('CHATY:','');
    const{data:c}=await sb.from('citizens').select('*').eq('citizen_id',cid).single();
    if(c){name=c.display_name||c.name;color=c.avatar_color||'#c9a84c';bio=c.bio||'';banner=c.banner_color||'#1a1c24';}else name=cid;
  }else{
    const{data:u}=await sb.from('chaty_users').select('*').eq('id',uid).single();
    if(u){targetUser=u;name=this._displayName(u,u.id);color=u.avatar_color;role=u.role||'user';bio=this._cleanBio(u);banner=u.banner_color||'#14161e';status=u.user_status||'online';warnings=Number(u.warnings)||0;muted=!!u.muted;banned=!!u.banned;muteReason=u.mute_reason||'';banReason=u.ban_reason||'';}
  }
  const canSeeStanding=plat!=='alyon'&&(this.isStaff()||uid===this._session?.id);
  const canModerate=plat==='chaty'&&this.isStaff()&&uid!==this._session?.id&&role!=='owner';
  const activeWarnings=plat==='alyon'?[]:await this._getActiveWarnings(uid);
  const standing=this._warningInfo({warnings,muted,banned,mute_reason:muteReason,ban_reason:banReason});
  const targetMeta=targetUser?userMeta(targetUser):{theme:'default',statusNote:''};
  const ov=document.createElement('div');ov.className='pp-overlay';
  const pp=document.createElement('div');pp.className=`profile-popup pf-theme-${cleanProfileTheme(targetMeta.theme||'default')}`;
  pp.innerHTML=`<div class="pp-banner" style="background:${banner}"></div><div class="pp-body"><button class="pp-close" onclick="this.closest('.profile-popup').remove();document.querySelector('.pp-overlay')?.remove()">X</button>${plat==='alyon'?this._avatarShell(initial(name),color,'pp-avatar','none'):this._avatarHtml(targetUser||{display_name:name,id:uid},color,'pp-avatar',name)}<div class="pp-name">${stDot(status)} ${esc(name)}</div><div class="pp-id">@${esc(uid.replace('CHATY:',''))}</div>${targetMeta.statusNote?`<div class="pp-bio">${esc(targetMeta.statusNote)}</div>`:''}${role!=='user'?`<div style="margin-top:4px"><span class="role-tag role-${role}">${role}</span></div>`:''}<div style="margin-top:6px"><span class="dc-plat-badge ${plat==='alyon'?'plat-alyon':'plat-chaty'}">${plat==='alyon'?'Alyon':'Chaty'}</span></div>${bio?`<div class="pp-bio">${esc(bio)}</div>`:''}${canSeeStanding?`<div class="pp-section"><div class="pf-section-title">ACCOUNT STANDING</div><div class="pp-mini"><span>State</span>${this._warningChip({warnings,muted,banned,mute_reason:muteReason,ban_reason:banReason})}</div><div class="pp-mini"><span>Warnings</span><strong>${standing.count}</strong></div><div class="pp-bio">${esc(standing.detail)}</div><div class="pf-warning-list">${this._renderWarningReasons(activeWarnings)}</div></div>`:''}${canModerate?`<div class="pp-section"><div class="pf-section-title">MOD PANEL</div><div class="pp-actions"><button class="btn btn-outline" onclick='App.warnUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Warn</button><button class="btn btn-outline" onclick='App.unwarnUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Unwarn</button><button class="btn btn-outline" onclick='App.tempMuteUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Temp Mute</button><button class="btn btn-outline" onclick='App.unmuteUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Unmute</button><button class="btn btn-outline" onclick='App.banUser(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>Ban</button><button class="btn btn-outline" onclick='App.startDm(${q(uid)});this.closest(".profile-popup").remove();document.querySelector(".pp-overlay")?.remove()'>DM</button></div></div>`:''}</div>`;
  ov.onclick=()=>{ov.remove();pp.remove();};
  document.body.appendChild(ov);
  document.body.appendChild(pp);
};

/* ===== DIHCORD V1.5+ CUSTOMIZATION PATCH ===== */
function cleanBannerFx(value){const fx=txt(value,'flow').toLowerCase();return['flow','slow','pulse','shimmer','none'].includes(fx)?fx:'flow';}
const __dihOldUserMeta=userMeta;
userMeta=function(user){const meta=__dihOldUserMeta(user);try{const source=String(user?.bio||'');const match=source.match(/^\[\[profile-meta\]\](\{.*?\})\[\[\/profile-meta\]\]\n?/s);if(match){const parsed=JSON.parse(match[1]||'{}');meta.bannerFx=cleanBannerFx(parsed.bannerFx||parsed.bannerMotion||meta.bannerFx);}}catch{}return meta;};
buildUserBio=function(cleanBio,meta){const payload={prefix:txt(meta?.prefix,'').slice(0,16),avatar:txt(meta?.avatar,'').slice(0,4),decor:txt(meta?.decor,'none').slice(0,16),avatarImg:txt(meta?.avatarImg||meta?.avatarImage,'').slice(0,500),frame:txt(meta?.frame,'none').slice(0,24),theme:txt(meta?.theme,'default').slice(0,24),statusNote:txt(meta?.statusNote,'').slice(0,64),bannerFx:cleanBannerFx(meta?.bannerFx||'flow')};const raw=JSON.stringify(payload);return `${META_OPEN}${raw}${META_CLOSE}\n${txt(cleanBio,'')}`.trim();};
App._applyWallpaper=function(){const url=txt(this._settings?.wallpaperUrl,'');const op=Math.min(.55,Math.max(0,Number(this._settings?.wallpaperOpacity??.22)||0));document.documentElement.style.setProperty('--chat-wallpaper',url?`url("${url.replace(/"/g,'%22')}")`:'none');document.documentElement.style.setProperty('--chat-wallpaper-opacity',String(op));document.documentElement.style.setProperty('--chat-motion-speed',this._settings?.animations===false?'0':'1');};
const __dihOldHydrate=App._hydrateUiPrefs;
App._hydrateUiPrefs=function(){__dihOldHydrate.call(this);this._settings={wallpaperUrl:'',wallpaperOpacity:.22,animations:true,themePreset:'custom',...(this._settings||{})};this._applyWallpaper();};
App.setWallpaper=function(){const url=(document.getElementById('site-wallpaper-url')?.value||'').trim().slice(0,900);const opacity=Number(document.getElementById('site-wallpaper-opacity')?.value||.22);this._settings.wallpaperUrl=url;this._settings.wallpaperOpacity=Math.min(.55,Math.max(0,opacity));this._persistSettings();this._applyWallpaper();this.goSettings();};
App.resetWallpaper=function(){this._settings.wallpaperUrl='';this._settings.wallpaperOpacity=.22;this._persistSettings();this._applyWallpaper();this.goSettings();};
App.toggleSmoothAnimations=function(value){this._settings.animations=value==='1';this._persistSettings();this._applyWallpaper();this.goSettings();};

/* ===== THEME STORE PATCH: OLD DISCORD ===== */
(function(){
  if(!document.getElementById('dih-theme-store-css')){
    const style=document.createElement('style');
    style.id='dih-theme-store-css';
    style.textContent=`
      .theme-store-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:12px;margin-top:10px}
      .theme-card{position:relative;overflow:hidden;padding:14px;border-radius:16px;border:1px solid rgba(255,255,255,.08);background:rgba(255,255,255,.035);cursor:pointer;transition:transform .18s ease,border-color .18s ease,background .18s ease}
      .theme-card:hover{transform:translateY(-2px);border-color:rgba(114,137,218,.55);background:rgba(255,255,255,.06)}
      .theme-card.active{border-color:var(--accent);box-shadow:0 0 0 1px rgba(114,137,218,.32),0 16px 35px rgba(0,0,0,.18)}
      .theme-preview{height:92px;border-radius:12px;overflow:hidden;border:1px solid rgba(0,0,0,.25);background:#36393f;display:grid;grid-template-columns:42px 1fr}
      .theme-preview-side{background:#2f3136;padding:9px 7px;display:flex;flex-direction:column;gap:6px}
      .theme-preview-pill{height:9px;border-radius:999px;background:#72767d;opacity:.75}
      .theme-preview-main{background:#36393f;padding:10px;display:flex;flex-direction:column;gap:8px}
      .theme-preview-line{height:9px;border-radius:999px;background:#b9bbbe;opacity:.55}
      .theme-preview-line.short{width:55%}.theme-preview-line.accent{width:72%;background:#7289da;opacity:.85}
      .theme-card-title{font-size:14px;font-weight:900;margin-top:10px}.theme-card-sub{font-size:12px;color:var(--t3);line-height:1.45;margin-top:4px}
      .theme-badge{position:absolute;top:10px;right:10px;font-family:var(--mono);font-size:9px;font-weight:800;letter-spacing:.8px;text-transform:uppercase;padding:3px 7px;border-radius:999px;background:rgba(114,137,218,.18);color:#b8c3ff;border:1px solid rgba(114,137,218,.3)}
      body.dih-preset-old-discord .dc-main{background:var(--bg2)!important}
      body.dih-preset-old-discord .dc-ch-header{background:#2f3136!important;box-shadow:none!important;border-bottom-color:#202225!important}
      body.dih-preset-old-discord .dc-server-card,body.dih-preset-old-discord .dc-home-hero,body.dih-preset-old-discord .site-hero,body.dih-preset-old-discord .forum-hero{background:#36393f!important;border-color:#202225!important;box-shadow:none!important}
      body.dih-preset-old-discord .dc-ch-item.dc-active,body.dih-preset-old-discord .dc-nav-item.dc-active{background:#42464d!important;color:#fff!important}
      body.dih-preset-old-discord .dc-input-shell{background:#40444b!important;border-color:#202225!important}
      body.dih-preset-old-discord .dc-msg-group:hover{background:rgba(4,4,5,.16)!important}
    `;
    document.head.appendChild(style);
  }
})();
const DIH_THEME_PRESETS={
  oldDiscord:{
    label:'Old Discord',
    desc:'Classic 2016-2019 Discord mood: blurple accent, dark panels, simple readable chat.',
    mode:'dark',
    wallpaperUrl:'',
    wallpaperOpacity:.18,
    vars:{bg:'#36393f',bg2:'#36393f',bg3:'#2f3136',bg4:'#40444b',bg5:'#2f3136',border:'#202225',soft:'#42464d',t1:'#dcddde',t2:'#b9bbbe',t3:'#72767d',accent:'#7289da',accent2:'#677bc4'}
  }
};
App._applyThemePreset=function(){
  const key=txt(this._settings?.themePreset,'custom');
  document.body.classList.remove('dih-preset-old-discord');
  Object.keys(DIH_THEME_PRESETS.oldDiscord.vars).forEach(v=>document.body.style.removeProperty(`--${v}`));
  if(key==='oldDiscord'){
    const p=DIH_THEME_PRESETS.oldDiscord;
    document.body.classList.add('dih-preset-old-discord');
    Object.entries(p.vars).forEach(([k,v])=>document.body.style.setProperty(`--${k}`,v));
  }
};
const __dihPresetApplyWallpaper=App._applyWallpaper;
App._applyWallpaper=function(){__dihPresetApplyWallpaper.call(this);this._applyThemePreset();};
App.applyThemePreset=function(key){
  if(key==='oldDiscord'){
    const p=DIH_THEME_PRESETS.oldDiscord;
    this._settings.themePreset='oldDiscord';
    this._settings.wallpaperUrl=p.wallpaperUrl;
    this._settings.wallpaperOpacity=p.wallpaperOpacity;
    this._persistSettings();
    this._applyTheme(p.mode);
    this._applyWallpaper();
    this.goSettings();
    return;
  }
  this._settings.themePreset='custom';
  this._persistSettings();
  this._applyWallpaper();
  this.goSettings();
};
App.themeStoreCardHtml=function(){
  const active=txt(this._settings?.themePreset,'custom');
  return `<div class="site-card" id="theme-store-card"><div class="site-card-head"><div><div class="site-card-title">Theme Store</div><div class="site-card-sub">Ready-made local themes</div></div><div class="site-actions"><button class="btn btn-outline" onclick="App.applyThemePreset('custom')">Custom</button></div></div><div class="theme-store-grid"><div class="theme-card ${active==='oldDiscord'?'active':''}" onclick="App.applyThemePreset('oldDiscord')"><span class="theme-badge">${active==='oldDiscord'?'Active':'Preset'}</span><div class="theme-preview"><div class="theme-preview-side"><div class="theme-preview-pill"></div><div class="theme-preview-pill"></div><div class="theme-preview-pill" style="background:#7289da"></div><div class="theme-preview-pill"></div></div><div class="theme-preview-main"><div class="theme-preview-line accent"></div><div class="theme-preview-line"></div><div class="theme-preview-line short"></div><div class="theme-preview-line"></div></div></div><div class="theme-card-title">Old Discord</div><div class="theme-card-sub">Classic dark panels, blurple buttons, and that old-school Discord vibe without nuking your layout.</div></div></div></div>`;
};

const __dihOldGoSettings=App.goSettings;
App.goSettings=function(){__dihOldGoSettings.call(this);const grid=document.querySelector('.site-grid');if(!grid||document.getElementById('wallpaper-card'))return;if(!document.getElementById('theme-store-card'))grid.insertAdjacentHTML('afterbegin',this.themeStoreCardHtml());grid.insertAdjacentHTML('afterbegin',`<div class="site-card" id="wallpaper-card"><div class="site-card-head"><div><div class="site-card-title">Chat Wallpaper & Motion</div><div class="site-card-sub">Local on this device</div></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Chat wallpaper URL</div><div class="site-row-sub">Paste an image link. Empty means default DIHCORD background.</div></div><div class="site-actions"><input id="site-wallpaper-url" class="form-input" style="min-width:260px" value="${attr(this._settings.wallpaperUrl||'')}" placeholder="https://.../wallpaper.png"></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Wallpaper opacity</div><div class="site-row-sub">Recommended: 0.15-0.30 so messages stay readable.</div></div><div class="site-actions"><input id="site-wallpaper-opacity" class="form-input site-select" type="number" min="0" max="0.55" step="0.05" value="${attr(this._settings.wallpaperOpacity??.22)}"></div></div><div class="site-row"><div class="site-row-copy"><div class="site-row-title">Smooth animations</div><div class="site-row-sub">Message pop-in, hover motion, animated banners and avatar frames.</div></div><div class="site-actions"><select class="form-input site-select" onchange="App.toggleSmoothAnimations(this.value)"><option value="1" ${this._settings.animations!==false?'selected':''}>On</option><option value="0" ${this._settings.animations===false?'selected':''}>Off</option></select></div></div><div class="site-actions" style="margin-top:10px"><button class="btn btn-accent" onclick="App.setWallpaper()">Apply Wallpaper</button><button class="btn btn-outline" onclick="App.resetWallpaper()">Reset</button></div></div>`);};
App._richTextHtml=function(raw){return String(raw||'').split(/\n/).map(line=>{const h2=line.match(/^##\s+(.+)/);const h1=line.match(/^#\s+(.+)/);if(h2)return `<div class="dc-md-h2">${rc(h2[1])}</div>`;if(h1)return `<div class="dc-md-h1">${rc(h1[1])}</div>`;return `<div class="dc-md-line">${rc(line)}</div>`;}).join('');};
App._messageHtml=function(m,myId){const image=parseImageContent(m?.content||'');if(image)return this._renderImageMessage(m);const poll=parsePollContent(m?.content||'');if(poll)return this._renderPoll(m,myId);return this._richTextHtml(m?.content||'');};
const __dihOldShowEditProfile=App.showEditProfile;
App.showEditProfile=async function(){await __dihOldShowEditProfile.call(this);const f=document.getElementById('edit-pf');if(!f||f.classList.contains('hidden')||document.getElementById('ep-banner-fx'))return;const meta=userMeta(this._me||{});const html=`<div><label class="form-label">Banner Motion</label><select id="ep-banner-fx" class="form-input"><option value="flow" ${cleanBannerFx(meta.bannerFx)==='flow'?'selected':''}>Flow</option><option value="slow" ${cleanBannerFx(meta.bannerFx)==='slow'?'selected':''}>Slow Flow</option><option value="pulse" ${cleanBannerFx(meta.bannerFx)==='pulse'?'selected':''}>Pulse</option><option value="shimmer" ${cleanBannerFx(meta.bannerFx)==='shimmer'?'selected':''}>Shimmer</option><option value="none" ${cleanBannerFx(meta.bannerFx)==='none'?'selected':''}>None</option></select></div>`;document.querySelector('#edit-pf .form-grid')?.insertAdjacentHTML('beforeend',html);};
App.saveProfile=async function(){if(!this._requireDb())return;const displayName=(document.getElementById('ep-dn').value.trim()||this._session.id).slice(0,this._maxNameLength);const prefix=(document.getElementById('ep-prefix').value.trim()||'').replace(/[^\w-]/g,'').slice(0,this._maxPrefixLength);const avatar=(document.getElementById('ep-avatar').value.trim()||'').slice(0,4);const decor=cleanAvatarDecor(document.getElementById('ep-decor').value||'none');const frame=cleanAvatarFrame(document.getElementById('ep-frame')?.value||'none');const theme=cleanProfileTheme(document.getElementById('ep-theme')?.value||'default');const bannerFx=cleanBannerFx(document.getElementById('ep-banner-fx')?.value||'flow');const statusNote=(document.getElementById('ep-note')?.value||'').trim().slice(0,64);const bio=document.getElementById('ep-bio').value.trim().slice(0,this._maxBioLength);let avatarImg=(document.getElementById('ep-avatar-img')?.value||'').trim();const file=document.getElementById('ep-avatar-file')?.files?.[0];const uploadMsg=document.getElementById('ep-upload-msg');if(file){if(uploadMsg)uploadMsg.textContent='Uploading avatar photo...';const uploaded=await this._uploadProfileAvatarAsset(file);if(!uploaded.ok){if(uploadMsg)uploadMsg.textContent=uploaded.error;alert(uploaded.error);return;}avatarImg=uploaded.src;}await sb.from('chaty_users').update({display_name:displayName,user_status:document.getElementById('ep-st').value,banner_color:document.getElementById('ep-bc').value,bio:buildUserBio(bio,{prefix,avatar,decor,avatarImg,frame,theme,statusNote,bannerFx})}).eq('id',this._session.id);this._session.name=displayName;localStorage.setItem('chaty_session',JSON.stringify(this._session));this.goProfile();};
const __dihOldGoProfile=App.goProfile;
App.goProfile=async function(){await __dihOldGoProfile.call(this);const meta=userMeta(this._me||{});const fx=cleanBannerFx(meta.bannerFx||'flow');if(fx!=='none')document.querySelector('.pf-banner')?.classList.add(`fx-${fx}`);};
const __dihOldShowProfile=App.showProfile;
App.showProfile=async function(uid,plat){await __dihOldShowProfile.call(this,uid,plat);const pp=document.querySelector('.profile-popup');if(!pp)return;let u=null;if(plat!=='alyon'){try{const r=await sb.from('chaty_users').select('bio').eq('id',uid).single();u=r.data;}catch{}}const meta=u?userMeta(u):{bannerFx:'flow'};const fx=cleanBannerFx(meta.bannerFx||'flow');if(fx!=='none')document.querySelector('.pp-banner')?.classList.add(`fx-${fx}`);};


/* ===== DIHCORD V21 MODERATION SHIELD: anti-bypass profanity + hate filter ===== */
(function(){
  if(!window.App)return;
  const SAFETY_VERSION='V21-MOD-SHIELD-ANTI-BYPASS';
  const ZERO_WIDTH=/[\u200B-\u200F\u202A-\u202E\u2060-\u206F\uFEFF]/g;
  const COMBINING=/[\u0300-\u036f]/g;
  const SEPARATORS=/[\s._\-~`'"“”‘’*•|\\\/()[\]{}<>:;,+^=!?]+/g;
  const decodeB64=(value)=>{
    try{
      const bin=atob(value);
      if(window.TextDecoder){return new TextDecoder('utf-8').decode(Uint8Array.from(bin,c=>c.charCodeAt(0)));}
      return decodeURIComponent(escape(bin));
    }catch(e){return '';}
  };
  const decodeList=(items)=>items.map(decodeB64).filter(Boolean);
  const PROFANITY_TERMS=decodeList([
    'ZnVjaw==','ZnVr','ZmNr','ZnZjaw==','c2hpdA==','Yml0Y2g=','YnRjaA==','YmljaA==','YXNzaG9sZQ==','YmFzdGFyZA==','bW90aGVyZnVja2Vy','ZGljaw==','Y3VudA==','c2x1dA==','d2hvcmU=','cmV0YXJk',
    '0YXRg9C5','0YXRg9C4','0YXRg9GP','0YXRg9C1','0YXQtdGA','0L/QuNC30LQ=','0L/Qt9C0','0L/QuNC30LTQtdGG','0LXQsQ==','0ZHQsQ==','0LXQsdCw','0LXQsdC7','0LXQsdC9','0LXQsdGD','0LXQsdC4','0LHQu9GP','0LHQu9GP0YLRjA==','0YHRg9C60LA=','0LzRg9C0','0LzRg9C00LDQug==','0LzRgNCw0Lc=','0LPQsNC90LTQvtC9','0LfQsNC70YPQvw==','0LTQvtC70LHQvtC10LE=','0LTQvtC70LHQsNC10LE=','0L/QuNC00L7RgA==',
    'eHV5','aHV5','aHVq','aHVp','cGl6ZA==','cHpk','cGl6ZGVj','ZWJhdA==','eWViYXQ=','ZWJs','ZWJu','Ymx5YQ==','c3VrYQ==','bXVkYWs=','cGlkb3I=','cGlkcg==','Z2FuZG9u','emFsdXBh','ZG9sYm9lYg=='
  ]);
  const HATE_TERMS=decodeList([
    'bmlnZ2Vy','bmlnZ2E=','bmlnYQ==','a2lrZQ==','Y2hpbms=','Z29vaw==','c3BpYw==','d2V0YmFjaw==','cmFnaGVhZA==','dG93ZWxoZWFk','c2FuZG5pZ2dlcg==','YmVhbmVy','Y29vbg==','aGVpbGhpdGxlcg==','d2hpdGVwb3dlcg==','Z2FzamV3cw==','a2lsbGpld3M=','a2lsbGJsYWNrcGVvcGxl','a2lsbG11c2xpbXM=','a2lsbGdheXBlb3BsZQ==','MTQ4OA==',
    '0L3QuNCz0LXRgA==','0L3QuNCz0LA=','0LbQuNC0','0LbQuNC00Ys=','0YfRg9GA0LrQsA==','0YfRg9GA0LrQuA==','0YXQsNGH','0YXQsNGH0Lg=','0YPQt9C60L7Qs9C70LDQtw==','0LfQuNCz0YXQsNC50LvRjA==','0LfQuNCz0YXQsNC50Ls='
  ]);
  const RISKY_TERMS=decodeList(['cG9ybg==','bnVkZXM=','ZG94eA==','ZG94','c3dhdA==','Z29yZQ==','bnNmdw==','Y3A=','Z3JhYmlmeQ==','aXBsb2dnZXI=','ZGlzY29yZGdpZnQ=','ZGlzY29yZC5naWZ0','Yml0bHk=','dGlueXVybA==','dGlueXVybGNvbQ==']);
  const TO_LATIN={
    'а':'a','е':'e','ё':'e','о':'o','р':'p','с':'c','х':'x','у':'y','к':'k','м':'m','т':'t','н':'h','в':'b','і':'i','ї':'i','ј':'j','ѕ':'s','з':'z','д':'d','л':'l','б':'b','ь':'b','я':'ya','ю':'yu','ш':'sh','щ':'sh','ч':'ch','ц':'c','ы':'y','и':'i','й':'i','г':'g','ф':'f','п':'p','ж':'zh','э':'e',
    '@':'a','4':'a','3':'e','1':'i','!':'i','|':'i','0':'o','$':'s','5':'s','7':'t','8':'b','+':'t'
  };
  const TO_CYR={
    'a':'а','@':'а','4':'а','e':'е','3':'е','o':'о','0':'о','p':'п','r':'р','c':'с','s':'с','$':'с','5':'с','x':'х','h':'х','u':'у','y':'у','k':'к','m':'м','t':'т','7':'т','b':'б','l':'л','i':'и','1':'и','!':'и','|':'и','d':'д','g':'г','f':'ф','v':'в','z':'з','q':'к','w':'в','j':'й'
  };
  const mapChars=(text,map)=>Array.from(text).map(ch=>map[ch]??ch).join('');
  const compact=(text)=>String(text||'').replace(SEPARATORS,'').replace(/[^a-zа-яё0-9]+/g,'');
  const squash=(text)=>String(text||'').replace(/(.)\1{1,}/g,'$1');
  const reverse=(text)=>Array.from(text).reverse().join('');
  const termKey=(term)=>squash(compact(mapChars(mapChars(String(term||'').normalize('NFKC').normalize('NFD').replace(COMBINING,'').toLowerCase(),TO_LATIN),TO_CYR)));

  App._safetyVersion=SAFETY_VERSION;
  App._safetyBase=function(text){
    return String(text||'')
      .normalize('NFKC')
      .normalize('NFD')
      .replace(COMBINING,'')
      .replace(ZERO_WIDTH,'')
      .replace(/&(?:nbsp|zwnj|zwj|#\d+|#x[0-9a-f]+);/gi,' ')
      .toLowerCase();
  };
  App._safetyVariants=function(text){
    const base=this._safetyBase(text);
    const latin=mapChars(base,TO_LATIN);
    const cyr=mapChars(base,TO_CYR);
    const raw=[base,latin,cyr,base.replace(SEPARATORS,''),latin.replace(SEPARATORS,''),cyr.replace(SEPARATORS,'')];
    const out=[];
    for(const value of raw){
      const v=String(value||'');
      const c=compact(v);
      const sq=squash(c);
      if(v.trim())out.push(v.trim());
      if(c)out.push(c);
      if(sq)out.push(sq);
      if(c.length>=4&&c.length<=80)out.push(reverse(c));
      if(sq.length>=4&&sq.length<=80)out.push(reverse(sq));
    }
    return [...new Set(out.filter(Boolean))].slice(0,80);
  };
  App._scanTermList=function(variants,terms){
    for(const term of terms){
      const raw=String(term||'');
      const keys=[termKey(raw),compact(mapChars(this._safetyBase(raw),TO_LATIN)),compact(mapChars(this._safetyBase(raw),TO_CYR))].filter(Boolean);
      for(const key of [...new Set(keys)]){
        if(key.length<3)continue;
        if(variants.some(v=>v.includes(key)))return true;
      }
    }
    return false;
  };
  App._scanUnsafeContent=function(text,options={}){
    const source=String(text||'');
    const normalized=this._safetyBase(source).replace(/\s+/g,' ').trim();
    if(!normalized)return{ok:false,msg:'Message is empty.'};
    const hidden=(source.match(ZERO_WIDTH)||[]).length;
    if(hidden>3)return{ok:false,msg:'Hidden unicode characters are blocked.'};
    const variants=this._safetyVariants(source);
    if(options.only!=='profanity'&&this._scanTermList(variants,HATE_TERMS))return{ok:false,msg:'Racist or hate speech is blocked on this server.'};
    if(options.only!=='hate'&&this._scanTermList(variants,PROFANITY_TERMS))return{ok:false,msg:'Profanity is blocked. Keep DIHCORD clean.'};
    if(!options.only&&this._scanTermList(variants,RISKY_TERMS))return{ok:false,msg:'That message looks unsafe for a school chat.'};
    return{ok:true};
  };
  App._normalizeText=function(value){return this._safetyBase(value).replace(/\s+/g,' ').trim();};
  App._messageNormalized=function(value){return squash(compact(mapChars(this._safetyBase(value),TO_LATIN)));};
  App._containsProfanity=function(text){return !this._scanUnsafeContent(text,{only:'hate'}).ok||!this._scanUnsafeContent(text,{only:'profanity'}).ok;};
  App._messageGuard=function(text){
    const normalized=this._normalizeText(text);
    if(!normalized)return{ok:false,msg:'Message is empty.'};
    if(String(text||'').length>this._maxMessageLength)return{ok:false,msg:`Message is too long. Max ${this._maxMessageLength} characters.`};
    if(/(.)\1{14,}/.test(String(text||'')))return{ok:false,msg:'Too many repeated characters.'};
    if(String(text||'').length>18&&String(text||'')===String(text||'').toUpperCase()&&/[A-ZА-ЯЁ]/.test(String(text||'')))return{ok:false,msg:'Too much CAPS. Relax a bit.'};
    const scan=this._scanUnsafeContent(text);
    if(!scan.ok)return scan;
    const variants=this._safetyVariants(text);
    if((this._riskyDomains||[]).some(domain=>variants.some(v=>v.includes(compact(String(domain||'').toLowerCase())))))return{ok:false,msg:'That link is blocked as risky.'};
    return{ok:true};
  };
  const oldBlocked=Array.isArray(App._blockedWords)?App._blockedWords:[];
  App._blockedWords=[...new Set([...oldBlocked,...RISKY_TERMS.filter(w=>w.length>2)])];
  const oldSaveProfile=App.saveProfile;
  App.saveProfile=async function(...args){
    const profileText=[
      document.getElementById('ep-dn')?.value||'',
      document.getElementById('ep-prefix')?.value||'',
      document.getElementById('ep-note')?.value||'',
      document.getElementById('ep-bio')?.value||''
    ].join(' ');
    const scan=this._scanUnsafeContent(profileText);
    if(!scan.ok){alert(scan.msg);return;}
    return oldSaveProfile.apply(this,args);
  };
})();

App.triggerFatalLock=function(reason){
  if(this._fatalLocked)return;
  this._fatalLocked=true;
  try{this._closeLiveSubs?.();}catch(e){}
  try{clearTimeout(this._typingTimer);}catch(e){}
  document.body.classList.add('fatal-lock');
  let overlay=document.getElementById('fatal-lock-screen');
  if(!overlay){
    overlay=document.createElement('div');
    overlay.id='fatal-lock-screen';
    overlay.className='fatal-lock-screen';
    document.body.appendChild(overlay);
  }
  const safeReason=esc((reason||'Unknown critical runtime failure').toString().slice(0,220));
  overlay.innerHTML=`<div class="fatal-lock-card"><div class="fatal-lock-kicker">Emergency Runtime Lock</div><div class="fatal-lock-title">CODE CORRUPTED</div><div class="fatal-lock-text">DIHCORD detected a critical code failure and locked the client to stop further damage or broken actions. This session cannot recover itself safely.</div><div class="fatal-lock-code">ERROR: ${safeReason}</div><div class="fatal-lock-note">Reload the page to restore the client</div></div>`;
  document.querySelectorAll('input,button,textarea,select').forEach(el=>{try{el.disabled=true;}catch(e){}});
};
for(const key of Object.keys(App)){
  const original=App[key];
  if(typeof original!=='function'||key==='triggerFatalLock')continue;
  if(original._fatalWrapped)continue;
  const wrapped=function(...args){
    if(App._fatalLocked)return;
    try{
      const result=original.apply(App,args);
      if(result&&typeof result.then==='function'){
        return result.catch(err=>{
          App.triggerFatalLock(err?.message||String(err||'Async failure'));
        });
      }
      return result;
    }catch(err){
      App.triggerFatalLock(err?.message||String(err||'Runtime failure'));
    }
  };
  wrapped._fatalWrapped=true;
  App[key]=wrapped;
}
window.addEventListener('error',event=>{
  App.triggerFatalLock(event?.error?.message||event?.message||'Script error');
});
window.addEventListener('unhandledrejection',event=>{
  const reason=event?.reason?.message||String(event?.reason||'Unhandled promise rejection');
  App.triggerFatalLock(reason);
});
</script>
<script id="dih-integrity-script">
(function(){
  const EXPECTED_SEAL='DIH-V15-LOCK-SEAL-20260414';
  function showIntegrityWarning(details){
    console.warn('[DIHCORD integrity]',details);
    window.__DIH_INTEGRITY_WARNING__=String(details||'unknown');
  }

  // P5 Web Editor rewrites/sandboxes HTML, so strict text-integrity checks can false-trigger.
  // This P5 build keeps the runtime guard, but integrity is warning-only instead of locking the client.
  const metaSeal=document.querySelector('meta[name="dih-lock-seal"]')?.getAttribute('content');
  if(metaSeal!==EXPECTED_SEAL)showIntegrityWarning('seal marker mismatch');

  const core=document.getElementById('dih-core-script');
  const guard=document.getElementById('dih-runtime-guard-script');
  if(!core)showIntegrityWarning('protected script missing dih-core-script');
  if(!guard)showIntegrityWarning('protected script missing dih-runtime-guard-script');

  if(window.App){
    const originalInit=App.init?.bind(App);
    if(originalInit&&!App._p5SafeInitWrapped){
      App._p5SafeInitWrapped=true;
      App.init=function(){
        return originalInit();
      };
    }
  }
})();
</script></body></html>
