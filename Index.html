import { useState, useEffect, useRef } from "react";

// ─── SEED DATA ────────────────────────────────────────────────────────────────
const INIT_EVENTS = [
  { id:"rtd2026", name:"Rocking the Daisies", type:"festival", banner:"🌼", color:"#c8f04a",
    dates:["2 Oct 2026","3 Oct 2026","4 Oct 2026"], dateIds:["fri","sat","sun"],
    venue:"Cloof Wine Estate, Darling", region:"Cape Town",
    description:"SA's favourite indie music & lifestyle festival set among the vines.",
    lineup:"Black Coffee · Tyla · SZA · Die Antwoord" },
  { id:"ultra2026", name:"Ultra South Africa", type:"festival", banner:"⚡", color:"#00d4ff",
    dates:["6 Feb 2026","7 Feb 2026"], dateIds:["sat","sun"],
    venue:"Expo Centre, Nasrec, Johannesburg", region:"Johannesburg",
    description:"The world's premier electronic music festival lands in Joburg.",
    lineup:"Martin Garrix · Tiësto · Amelie Lens" },
  { id:"derby2026", name:"Soweto Derby 2026", type:"sports", banner:"⚽", color:"#f0a030",
    dates:["18 Apr 2026"], dateIds:["sat"],
    venue:"FNB Stadium, Nasrec", region:"Johannesburg",
    description:"Kaizer Chiefs vs Orlando Pirates. The biggest match in SA football.", lineup:null },
  { id:"coldplay2026", name:"Coldplay: Music of the Spheres", type:"concert", banner:"🌌", color:"#a78bfa",
    dates:["11 Mar 2026","12 Mar 2026"], dateIds:["wed","thu"],
    venue:"DHL Newlands Stadium, Cape Town", region:"Cape Town",
    description:"One of the world's biggest live acts returns to Cape Town.", lineup:null },
  { id:"capejazz2026", name:"Cape Town Jazz Festival", type:"festival", banner:"🎷", color:"#f472b6",
    dates:["27 Mar 2026","28 Mar 2026"], dateIds:["fri","sat"],
    venue:"CTICC, Cape Town", region:"Cape Town",
    description:"Africa's largest jazz gathering. Two stages, world-class artists.",
    lineup:"Zakes Bantwini · Thandiswa Mazwai" },
];

const INIT_OPERATORS = [
  { id:"op1", name:"Cape Roller Shuttles", logo:"🚐", status:"verified", rating:4.8, reviews:134,
    owner:{ name:"Sipho Dlamini", id_number:"8501015026083", phone:"+27821000001", email:"sipho@caperoller.co.za" },
    docs:{ cipc:"submitted", pdp:"submitted", roadworthy:"submitted", id_copy:"submitted", selfie:"submitted" },
    drivers:[
      { id:"d1", name:"Sipho Dlamini", pdp:"PDP123456", phone:"+27821000001", photo:"👨🏾", status:"verified" },
      { id:"d2", name:"Ayanda Mokoena", pdp:"PDP654321", phone:"+27821000099", photo:"👨🏿", status:"verified" },
    ],
    vehicles:[
      { id:"v1", plate:"CA 123-456", make:"Toyota Quantum", seats:16, colour:"White", roadworthy:"2027-01", status:"verified" },
      { id:"v2", plate:"CA 789-012", make:"Hyundai H1", seats:10, colour:"Silver", roadworthy:"2026-08", status:"verified" },
    ],
    description:"Air-conditioned Quantums. Ice cold water on board.", whatsapp:"+27821000001", balance:4200 },
  { id:"op2", name:"Daisy Runners", logo:"🌼", status:"verified", rating:4.5, reviews:89,
    owner:{ name:"Lerato Nkosi", id_number:"9203045026083", phone:"+27821000002", email:"lerato@daisyrunners.co.za" },
    docs:{ cipc:"submitted", pdp:"submitted", roadworthy:"submitted", id_copy:"submitted", selfie:"submitted" },
    drivers:[{ id:"d3", name:"Lerato Nkosi", pdp:"PDP789012", phone:"+27821000002", photo:"👩🏽", status:"verified" }],
    vehicles:[{ id:"v3", plate:"CA 456-789", make:"Toyota Hiace", seats:22, colour:"Yellow", roadworthy:"2026-11", status:"verified" }],
    description:"Budget-friendly 22-seaters. On-time or 10% refund.", whatsapp:"+27821000002", balance:1850 },
];

const INIT_LISTINGS = [
  { id:"l1", operatorId:"op1", eventId:"rtd2026", location:"Cape Town Airport", direction:"to", dateId:"fri", date:"2 Oct 2026", time:"07:00", price:350, seatsTotal:16, seatsLeft:9, driverId:"d1", vehicleId:"v1", amenities:["ac","water","music"] },
  { id:"l2", operatorId:"op1", eventId:"rtd2026", location:"Bellville", direction:"to", dateId:"fri", date:"2 Oct 2026", time:"09:00", price:180, seatsTotal:16, seatsLeft:14, driverId:"d2", vehicleId:"v1", amenities:["ac","water"] },
  { id:"l3", operatorId:"op1", eventId:"rtd2026", location:"Cape Town Airport", direction:"from", dateId:"sun", date:"4 Oct 2026", time:"18:00", price:390, seatsTotal:16, seatsLeft:5, driverId:"d1", vehicleId:"v2", amenities:["ac","water","music"] },
  { id:"l4", operatorId:"op2", eventId:"rtd2026", location:"Paarl", direction:"to", dateId:"sat", date:"3 Oct 2026", time:"08:30", price:130, seatsTotal:22, seatsLeft:18, driverId:"d3", vehicleId:"v3", amenities:["ac"] },
  { id:"l5", operatorId:"op2", eventId:"ultra2026", location:"Sandton City", direction:"to", dateId:"sat", date:"6 Feb 2026", time:"14:00", price:120, seatsTotal:22, seatsLeft:11, driverId:"d3", vehicleId:"v3", amenities:["ac","music"] },
  { id:"l6", operatorId:"op1", eventId:"coldplay2026", location:"Cape Town CBD", direction:"to", dateId:"wed", date:"11 Mar 2026", time:"17:00", price:80, seatsTotal:16, seatsLeft:12, driverId:"d1", vehicleId:"v1", amenities:["ac","water"] },
];

const INIT_RIDERS = [
  { id:"r1", name:"Thabo Sithole", email:"thabo@example.com", phone:"+27831000001",
    status:"verified", id_number:"9506015026083", selfie:"👨🏾", bookings:8, flags:0,
    cards:[{ id:"c1", type:"visa", last4:"4242", expiry:"08/27", name:"THABO SITHOLE", primary:true }],
    savedEvents:["rtd2026","ultra2026"], notifications:{ bookingUpdates:true, promos:false, reminders:true } },
];

const INIT_BOOKINGS = [
  { id:"b1", listingId:"l1", riderId:"r1", riderName:"Thabo Sithole", riderPhone:"+27831000001",
    seats:2, total:700, status:"confirmed", created:"2026-03-10T10:22:00", expiresAt:"2026-03-11T10:22:00", paymentStatus:"released" },
  { id:"b2", listingId:"l3", riderId:"r1", riderName:"Thabo Sithole", riderPhone:"+27831000001",
    seats:1, total:390, status:"pending_confirmation", created:"2026-03-15T10:22:00", expiresAt:"2026-03-16T10:22:00", paymentStatus:"held" },
];

const INIT_REVIEWS = [
  { id:"rv1", operatorId:"op1", riderId:"r1", riderName:"Thabo S.", rating:5, comment:"Sipho was on time and the Quantum was clean and cold. Best shuttle experience!", date:"2026-03-12", bookingId:"b1" },
  { id:"rv2", operatorId:"op2", riderId:"r1", riderName:"Thabo S.", rating:4, comment:"Good value, slight delay but driver communicated well.", date:"2026-02-20", bookingId:null },
];

// ─── CONSTANTS ────────────────────────────────────────────────────────────────
const TYPE_META = {
  festival:{ label:"Festival", icon:"🎪", color:"#c8f04a" },
  sports:  { label:"Sports",  icon:"🏟️", color:"#f0a030" },
  concert: { label:"Concert", icon:"🎤", color:"#a78bfa" },
};
const AMENITY_ICONS = { ac:"❄️", water:"💧", music:"🎵", wifi:"📶", usb:"🔌", snacks:"🍿" };
const BOOKING_STATUS = {
  pending_confirmation:{ label:"⏳ Awaiting Confirmation", color:"#fbbf24" },
  confirmed:           { label:"✓ Confirmed",              color:"#4ade80" },
  declined:            { label:"✗ Declined",               color:"#f87171" },
  completed:           { label:"✓ Completed",              color:"#6ee7b7" },
  cancelled:           { label:"✗ Cancelled",              color:"#9ca3af" },
};
const STATUS_COLORS = { verified:"#4ade80", docs_submitted:"#fbbf24", pending:"#fbbf24", rejected:"#f87171", id_submitted:"#fbbf24", unverified:"#f87171" };
const STATUS_LABELS = { verified:"✓ Verified", docs_submitted:"⏳ Docs Submitted", pending:"⏳ Pending", rejected:"✗ Rejected", id_submitted:"⏳ ID Submitted", unverified:"○ Unverified" };

// ─── HELPERS ──────────────────────────────────────────────────────────────────
function stars(n) { return n ? "★".repeat(Math.round(n))+"☆".repeat(5-Math.round(n)) : "☆☆☆☆☆"; }
function hoursLeft(iso) { const h=Math.round((new Date(iso)-new Date("2026-03-15T18:00:00"))/36e5); return Math.max(0,h); }
function formatCardNum(v){ return v.replace(/\D/g,"").slice(0,16).replace(/(.{4})/g,"$1 ").trim(); }
function formatExpiry(v){ const d=v.replace(/\D/g,"").slice(0,4); return d.length>2?d.slice(0,2)+"/"+d.slice(2):d; }
function detectCardType(n){ const r=n.replace(/\s/g,""); return r.startsWith("4")?"visa":r.startsWith("5")?"mastercard":r.startsWith("3")?"amex":"card"; }

// ─── APP ROOT ─────────────────────────────────────────────────────────────────
export default function App() {
  const [screen, setScreen]       = useState("home");
  const [events, setEvents]       = useState(INIT_EVENTS);
  const [operators, setOperators] = useState(INIT_OPERATORS);
  const [listings, setListings]   = useState(INIT_LISTINGS);
  const [riders, setRiders]       = useState(INIT_RIDERS);
  const [bookings, setBookings]   = useState(INIT_BOOKINGS);
  const [reviews, setReviews]     = useState(INIT_REVIEWS);
  const [activeTab, setActiveTab] = useState("home");
  const [activeEventId, setActiveEventId] = useState(null);
  const [bookTarget, setBookTarget] = useState(null);
  const [toast, setToast]         = useState(null);
  const [searchQ, setSearchQ]     = useState("");
  const RIDER_ID = "r1";

  const ctx = { events, setEvents, operators, setOperators, listings, setListings, riders, setRiders, bookings, setBookings, reviews, setReviews, RIDER_ID };

  function showToast(msg, type="success") { setToast({ msg, type }); setTimeout(()=>setToast(null), 3000); }
  function nav(tab, scr) { setActiveTab(tab); setScreen(scr || tab); }

  const activeEvent = events.find(e => e.id === activeEventId);

  return (
    <div style={S.root}>
      <style>{GLOBAL_CSS}</style>

      {/* TOAST */}
      {toast && (
        <div style={{ ...S.toast, background: toast.type==="error"?"#2a0a0a":toast.type==="warn"?"#1a1400":"#0d1f0d", borderColor: toast.type==="error"?"#f8717155":toast.type==="warn"?"#fbbf2455":"#4ade8055", color: toast.type==="error"?"#f87171":toast.type==="warn"?"#fbbf24":"#4ade80" }}>
          {toast.type==="error"?"✗":toast.type==="warn"?"⚠️":"✓"} {toast.msg}
        </div>
      )}

      {/* NAV */}
      <nav style={S.nav}>
        <button onClick={() => nav("home")} style={S.navBrand}>
          <span style={S.logoBox}>S</span>
          <span style={S.logoWord}>SHUTTLR</span>
        </button>
        <div style={S.navLinks}>
          {[
            ["home","🏠","Home"],
            ["events","🎫","Events"],
            ["account","👤","My Account"],
            ["operator","🚐","Operators"],
            ["admin","⚙️","Admin"],
          ].map(([t,ic,lb]) => (
            <button key={t} onClick={() => nav(t)} style={{ ...S.navBtn, ...(activeTab===t?S.navBtnActive:{}) }}>
              <span style={S.navBtnIcon}>{ic}</span>
              <span style={S.navBtnLabel}>{lb}</span>
            </button>
          ))}
        </div>
      </nav>

      <div style={S.wrap}>
        {screen==="home"     && <HomeScreen ctx={ctx} setScreen={setScreen} setActiveEventId={setActiveEventId} nav={nav} searchQ={searchQ} setSearchQ={setSearchQ} showToast={showToast} />}
        {screen==="events"   && <EventsScreen ctx={ctx} setScreen={setScreen} setActiveEventId={setActiveEventId} searchQ={searchQ} setSearchQ={setSearchQ} showToast={showToast} />}
        {screen==="event"    && activeEvent && <EventScreen event={activeEvent} ctx={ctx} setScreen={setScreen} setBookTarget={setBookTarget} showToast={showToast} />}
        {screen==="book"     && bookTarget  && <BookScreen target={bookTarget} ctx={ctx} setScreen={setScreen} showToast={showToast} />}
        {screen==="account"  && <AccountScreen ctx={ctx} setScreen={setScreen} showToast={showToast} />}
        {screen==="operator" && <OperatorScreen ctx={ctx} setScreen={setScreen} showToast={showToast} />}
        {screen==="op_reg"   && <OperatorRegScreen ctx={ctx} setScreen={setScreen} showToast={showToast} />}
        {screen==="admin"    && <AdminScreen ctx={ctx} showToast={showToast} />}
        {screen==="verify"   && <VerifyRiderScreen ctx={ctx} setScreen={setScreen} showToast={showToast} />}
      </div>

      {/* BOTTOM NAV (mobile) */}
      <div style={S.bottomNav}>
        {[["home","🏠","Home"],["events","🎫","Events"],["account","👤","Me"],["operator","🚐","Ops"],["admin","⚙️","Admin"]].map(([t,ic,lb])=>(
          <button key={t} onClick={() => nav(t)} style={{ ...S.bnBtn, ...(activeTab===t?S.bnBtnActive:{}) }}>
            <span style={{ fontSize:18 }}>{ic}</span>
            <span style={{ fontSize:10, marginTop:2 }}>{lb}</span>
          </button>
        ))}
      </div>

      <footer style={S.footer}>© 2026 Shuttlr · Event Transport Marketplace · Payments held in escrow</footer>
    </div>
  );
}

// ─── HOME SCREEN ──────────────────────────────────────────────────────────────
function HomeScreen({ ctx, setScreen, setActiveEventId, nav, searchQ, setSearchQ, showToast }) {
  const { events, listings, riders, RIDER_ID } = ctx;
  const rider = riders.find(r=>r.id===RIDER_ID);
  const upcomingEvents = events.slice(0,3);
  const totalListings = listings.length;
  const verifiedOps = ctx.operators.filter(o=>o.status==="verified").length;

  function goEvent(id) { setActiveEventId(id); setScreen("event"); nav("events"); }

  return (
    <div style={S.page}>
      {/* Hero */}
      <div style={S.hero}>
        <div style={S.heroBg} />
        <p style={S.heroEye}>Festival · Concert · Sports · Live Events</p>
        <h1 style={S.heroH1}>YOUR RIDE<br/>TO THE ACTION</h1>
        <p style={S.heroSub}>Verified operators. Verified drivers. Secure escrow payments.</p>
        <div style={S.heroSearch}>
          <span style={S.heroSearchIcon}>🔍</span>
          <input style={S.heroSearchInp} placeholder="Search events, venues, cities…"
            value={searchQ} onChange={e=>setSearchQ(e.target.value)}
            onFocus={()=>nav("events")} />
        </div>
        <div style={S.heroStats}>
          <div style={S.heroStat}><span style={S.heroStatNum}>{events.length}</span><span style={S.heroStatLbl}>Events</span></div>
          <div style={S.heroStatDiv} />
          <div style={S.heroStat}><span style={S.heroStatNum}>{verifiedOps}</span><span style={S.heroStatLbl}>Verified Operators</span></div>
          <div style={S.heroStatDiv} />
          <div style={S.heroStat}><span style={S.heroStatNum}>{totalListings}</span><span style={S.heroStatLbl}>Active Shuttles</span></div>
        </div>
      </div>

      {/* Trust strip */}
      <div style={S.trustStrip}>
        {[["🔒","Escrow Payments","Funds held until driver confirms"],["🪪","ID Verified Riders","Every passenger identity checked"],["✅","Vetted Operators","CIPC, PDP & roadworthy checked"],["⏱","24h Confirm","Auto-refund if no response"]].map(([ic,t,s])=>(
          <div key={t} style={S.trustItem}>
            <span style={S.trustIcon}>{ic}</span>
            <div><div style={S.trustTitle}>{t}</div><div style={S.trustSub}>{s}</div></div>
          </div>
        ))}
      </div>

      {/* Saved events */}
      {rider?.savedEvents?.length > 0 && (
        <div style={S.section}>
          <SHead title="Your Saved Events" action={{ label:"See all →", onClick:()=>nav("events") }} />
          <div style={S.eventGrid}>
            {events.filter(e=>rider.savedEvents.includes(e.id)).map(e=>(
              <EventCard key={e.id} ev={e} onClick={()=>goEvent(e.id)} ctx={ctx} RIDER_ID={RIDER_ID} showToast={showToast} />
            ))}
          </div>
        </div>
      )}

      {/* Upcoming events */}
      <div style={S.section}>
        <SHead title="Upcoming Events" action={{ label:"Browse all →", onClick:()=>nav("events") }} />
        <div style={S.eventGrid}>
          {upcomingEvents.map(e=>(
            <EventCard key={e.id} ev={e} onClick={()=>goEvent(e.id)} ctx={ctx} RIDER_ID={RIDER_ID} showToast={showToast} />
          ))}
        </div>
      </div>

      {/* How it works */}
      <div style={S.section}>
        <SHead title="How Shuttlr Works" />
        <div style={S.howGrid}>
          {[["1","Find an Event","Browse festivals, concerts and sports matches near you.","🎫"],
            ["2","Compare Shuttles","Multiple operators compete on price, rating and amenities.","🚐"],
            ["3","Book & Pay","Payment held securely in escrow until your seat is confirmed.","🔒"],
            ["4","Ride Safe","Every driver, vehicle and passenger is ID-verified.","✅"]].map(([n,t,d,ic])=>(
            <div key={n} style={S.howCard}>
              <div style={S.howNum}>{n}</div>
              <span style={{ fontSize:32, marginBottom:10, display:"block" }}>{ic}</span>
              <div style={S.howTitle}>{t}</div>
              <div style={S.howDesc}>{d}</div>
            </div>
          ))}
        </div>
      </div>
    </div>
  );
}

// ─── EVENTS SCREEN ────────────────────────────────────────────────────────────
function EventsScreen({ ctx, setScreen, setActiveEventId, searchQ, setSearchQ, showToast }) {
  const { events, listings, RIDER_ID, riders } = ctx;
  const [filterType, setFilterType] = useState("all");
  const [filterRegion, setFilterRegion] = useState("all");
  const regions = ["all",...Array.from(new Set(events.map(e=>e.region)))];

  const filtered = events.filter(e=>
    (filterType==="all"||e.type===filterType) &&
    (filterRegion==="all"||e.region===filterRegion) &&
    (!searchQ||e.name.toLowerCase().includes(searchQ.toLowerCase())||e.venue.toLowerCase().includes(searchQ.toLowerCase()))
  );

  function goEvent(id) { setActiveEventId(id); setScreen("event"); }

  return (
    <div style={S.page}>
      <SHead title="All Events" sub={`${filtered.length} event${filtered.length!==1?"s":""} available`} />
      <div style={S.searchRow}>
        <div style={S.searchBox}>
          <span style={{ position:"absolute", left:12, top:"50%", transform:"translateY(-50%)" }}>🔍</span>
          <input style={S.searchInp} placeholder="Search events or venues…" value={searchQ} onChange={e=>setSearchQ(e.target.value)} />
          {searchQ && <button style={S.searchClear} onClick={()=>setSearchQ("")}>✕</button>}
        </div>
      </div>
      <div style={S.filterBlock}>
        <FilterRow label="Type">
          {["all","festival","sports","concert"].map(t=>(
            <Pill key={t} active={filterType===t} onClick={()=>setFilterType(t)}>
              {t==="all"?"All":TYPE_META[t].icon+" "+TYPE_META[t].label}
            </Pill>
          ))}
        </FilterRow>
        <FilterRow label="Region">
          {regions.map(r=><Pill key={r} active={filterRegion===r} onClick={()=>setFilterRegion(r)}>{r==="all"?"All Regions":"📍 "+r}</Pill>)}
        </FilterRow>
      </div>
      {filtered.length===0
        ? <Empty icon="🎫" msg="No events match your search." />
        : <div style={S.eventGrid}>
            {filtered.map(e=><EventCard key={e.id} ev={e} onClick={()=>goEvent(e.id)} ctx={ctx} RIDER_ID={RIDER_ID} showToast={showToast} />)}
          </div>
      }
    </div>
  );
}

function EventCard({ ev, onClick, ctx, RIDER_ID, showToast }) {
  const { listings, riders, setRiders } = ctx;
  const rider = riders.find(r=>r.id===RIDER_ID);
  const saved = rider?.savedEvents?.includes(ev.id);
  const evListings = listings.filter(l=>l.eventId===ev.id);
  const lowestPrice = evListings.length ? Math.min(...evListings.map(l=>l.price)) : null;
  const tm = TYPE_META[ev.type];

  function toggleSave(e) {
    e.stopPropagation();
    setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,
      savedEvents: saved ? r.savedEvents.filter(id=>id!==ev.id) : [...(r.savedEvents||[]), ev.id]
    }));
    showToast(saved?"Event removed from saved":"Event saved!");
  }

  return (
    <div className="ev-card" onClick={onClick} style={{ ...S.evCard, borderTop:`3px solid ${ev.color}` }}>
      <div style={S.evCardTop}>
        <span style={{ fontSize:36 }}>{ev.banner}</span>
        <div style={{ display:"flex", gap:6, alignItems:"center" }}>
          <span style={{ ...S.typePill, background:tm.color+"22", color:tm.color, border:`1px solid ${tm.color}44` }}>{tm.icon} {tm.label}</span>
          <button onClick={toggleSave} style={{ ...S.saveBtn, color: saved?"#f87171":"#555" }}>{saved?"♥":"♡"}</button>
        </div>
      </div>
      <h3 style={S.evName}>{ev.name}</h3>
      <p style={S.evVenue}>📍 {ev.venue}</p>
      <p style={S.evDates}>🗓 {ev.dates.join(" · ")}</p>
      {ev.lineup && <p style={S.evLineup}>🎵 {ev.lineup}</p>}
      <div style={S.evFoot}>
        <span style={{ color:ev.color, fontSize:12, fontWeight:600 }}>
          {evListings.length>0 ? `🚐 ${evListings.length} shuttle${evListings.length!==1?"s":""} from R${lowestPrice}` : "🕐 Shuttles coming soon"}
        </span>
        <span style={{ fontSize:12, color:"#444" }}>View →</span>
      </div>
    </div>
  );
}

// ─── EVENT SCREEN ─────────────────────────────────────────────────────────────
function EventScreen({ event, ctx, setScreen, setBookTarget, showToast }) {
  const { listings, operators, reviews } = ctx;
  const [filterDir, setFilterDir]   = useState("all");
  const [filterDate, setFilterDate] = useState("all");
  const [filterLoc, setFilterLoc]   = useState("all");
  const [sortBy, setSortBy]         = useState("price");
  const [priceMax, setPriceMax]     = useState(1000);

  const evListings = listings.filter(l=>l.eventId===event.id);
  const locations = ["all",...Array.from(new Set(evListings.map(l=>l.location)))];
  const evReviews = reviews.filter(r=>operators.find(o=>o.id===r.operatorId && evListings.find(l=>l.operatorId===o.id)));

  const filtered = evListings
    .filter(l=>{
      const op = operators.find(o=>o.id===l.operatorId);
      return op?.status==="verified" &&
        (filterDir==="all"||l.direction===filterDir) &&
        (filterDate==="all"||l.dateId===filterDate) &&
        (filterLoc==="all"||l.location===filterLoc) &&
        l.price<=priceMax && l.seatsLeft>0;
    })
    .sort((a,b)=>sortBy==="price"?a.price-b.price:operators.find(o=>o.id===b.operatorId)?.rating-operators.find(o=>o.id===a.operatorId)?.rating);

  return (
    <div style={S.page}>
      <button onClick={()=>setScreen("events")} style={S.backBtn}>← All Events</button>

      {/* Event Hero */}
      <div style={{ ...S.evHero, borderBottom:`1px solid ${event.color}22` }}>
        <span style={{ fontSize:60, flexShrink:0 }}>{event.banner}</span>
        <div style={{ flex:1 }}>
          <div style={{ display:"flex", gap:8, flexWrap:"wrap", marginBottom:8 }}>
            <span style={{ ...S.typePill, background:TYPE_META[event.type].color+"22", color:TYPE_META[event.type].color, border:`1px solid ${TYPE_META[event.type].color}44` }}>{TYPE_META[event.type].icon} {TYPE_META[event.type].label}</span>
            <span style={{ ...S.typePill, background:"#ffffff0a", color:"#666" }}>📍 {event.region}</span>
          </div>
          <h1 style={{ ...S.evHeroTitle, color:event.color }}>{event.name}</h1>
          <p style={S.evHeroMeta}>{event.venue}</p>
          <p style={S.evHeroMeta}>{event.dates.join(" · ")}</p>
          {event.lineup && <p style={{ ...S.evHeroMeta, color:"#777", fontStyle:"italic" }}>🎵 {event.lineup}</p>}
          <p style={{ color:"#555", fontSize:14, marginTop:8, lineHeight:1.6 }}>{event.description}</p>
        </div>
      </div>

      {/* Price range */}
      <div style={S.priceRangeBar}>
        <span style={{ fontSize:12, color:"#555" }}>Max price: <strong style={{ color:"#c8f04a" }}>R{priceMax}</strong></span>
        <input type="range" min={50} max={1000} step={10} value={priceMax} onChange={e=>setPriceMax(+e.target.value)} style={S.rangeSlider} />
      </div>

      {/* Filters */}
      <div style={S.filterBlock}>
        <FilterRow label="Direction">
          {[["all","All"],["to","→ To Event"],["from","← From Event"]].map(([v,l])=>(
            <Pill key={v} active={filterDir===v} onClick={()=>setFilterDir(v)}>{l}</Pill>
          ))}
        </FilterRow>
        <FilterRow label="Date">
          <Pill active={filterDate==="all"} onClick={()=>setFilterDate("all")}>All Dates</Pill>
          {event.dates.map((d,i)=><Pill key={i} active={filterDate===event.dateIds[i]} onClick={()=>setFilterDate(event.dateIds[i])}>{d}</Pill>)}
        </FilterRow>
        <FilterRow label="Pick-up">
          {locations.map(l=><Pill key={l} active={filterLoc===l} onClick={()=>setFilterLoc(l)}>{l==="all"?"All":l}</Pill>)}
        </FilterRow>
        <FilterRow label="Sort">
          <Pill active={sortBy==="price"} onClick={()=>setSortBy("price")}>💰 Cheapest</Pill>
          <Pill active={sortBy==="rating"} onClick={()=>setSortBy("rating")}>⭐ Top Rated</Pill>
        </FilterRow>
      </div>

      <div style={{ color:"#555", fontSize:13, marginBottom:14 }}>{filtered.length} shuttle{filtered.length!==1?"s":""} found</div>

      {filtered.length===0
        ? <Empty icon="🚌" msg="No shuttles match your filters." />
        : <div style={{ display:"flex", flexDirection:"column", gap:12 }}>
            {filtered.map(l=><ShuttleCard key={l.id} listing={l} event={event} ctx={ctx} onBook={()=>{ setBookTarget({listing:l, event}); setScreen("book"); }} />)}
          </div>
      }

      {/* Reviews */}
      {evReviews.length>0 && (
        <div style={{ marginTop:40 }}>
          <SHead title="Recent Reviews" sub="From verified riders on this event" />
          <div style={{ display:"flex", flexDirection:"column", gap:10 }}>
            {evReviews.slice(0,3).map(r=><ReviewCard key={r.id} review={r} />)}
          </div>
        </div>
      )}
    </div>
  );
}

function ShuttleCard({ listing, event, ctx, onBook }) {
  const { operators } = ctx;
  const op = operators.find(o=>o.id===listing.operatorId);
  const driver = op?.drivers.find(d=>d.id===listing.driverId);
  const vehicle = op?.vehicles.find(v=>v.id===listing.vehicleId);
  const low = listing.seatsLeft <= 3;

  return (
    <div className="lst-card" style={S.lstCard}>
      <div style={{ ...S.lstAccent, background:event.color }} />
      <div style={S.lstBody}>
        {/* Top */}
        <div style={S.lstTop}>
          <div style={S.lstOpRow}>
            <span style={{ fontSize:26 }}>{op?.logo}</span>
            <div>
              <div style={{ fontWeight:700, fontSize:15, display:"flex", gap:6, alignItems:"center" }}>
                {op?.name}
                <StatusBadge status={op?.status} small />
              </div>
              <div style={{ color:"#f0a030", fontSize:12 }}>{stars(op?.rating)} {op?.rating} ({op?.reviews})</div>
            </div>
          </div>
          <div style={S.lstPriceCol}>
            <span style={{ ...S.lstPrice, color:event.color }}>R{listing.price}</span>
            <span style={S.lstPP}>per person</span>
          </div>
        </div>

        {/* Route */}
        <div style={S.lstRoute}>
          <span style={S.lstLocChip}>📍 {listing.location}</span>
          <span style={{ color:event.color, fontWeight:700, fontSize:13 }}>{listing.direction==="to"?`→ ${event.name}`:`← ${event.name}`}</span>
        </div>
        <div style={S.lstMeta}>
          <span>📅 {listing.date}</span>
          <span>🕐 {listing.time}</span>
          <span style={{ color: low?"#f87171":"#4ade80" }}>{low?`⚠️ ${listing.seatsLeft} left`:`✓ ${listing.seatsLeft} seats`}</span>
        </div>

        {/* Amenities */}
        {listing.amenities?.length>0 && (
          <div style={S.amenityRow}>
            {listing.amenities.map(a=>(
              <span key={a} style={S.amenityChip}>{AMENITY_ICONS[a]||"•"} {a.toUpperCase()}</span>
            ))}
          </div>
        )}

        {/* Driver & vehicle strip */}
        <div style={S.driverVehicleStrip}>
          {driver && (
            <div style={S.dvItem}>
              <div style={S.dvAvatar}>{driver.photo}</div>
              <div><div style={{ fontSize:12, fontWeight:600 }}>{driver.name}</div><div style={{ fontSize:11, color:"#555" }}>PDP ✓</div></div>
            </div>
          )}
          {vehicle && (
            <div style={S.dvItem}>
              <span style={{ fontSize:20 }}>🚐</span>
              <div><div style={{ fontSize:12, fontWeight:600 }}>{vehicle.plate}</div><div style={{ fontSize:11, color:"#555" }}>{vehicle.make}</div></div>
            </div>
          )}
          <div style={{ ...S.dvItem, marginLeft:"auto" }}>
            <span style={{ fontSize:16 }}>🔒</span>
            <div style={{ fontSize:11, color:"#555" }}>Escrow</div>
          </div>
        </div>

        <div style={S.lstBtns}>
          <a href={`https://wa.me/${op?.whatsapp?.replace(/\D/g,"")}`} target="_blank" rel="noreferrer" style={S.waBtn}>💬 WhatsApp</a>
          <button className="book-btn" style={{ ...S.bookBtn, background:event.color }} onClick={onBook}>Book Now →</button>
        </div>
      </div>
    </div>
  );
}

// ─── BOOK SCREEN ──────────────────────────────────────────────────────────────
function BookScreen({ target, ctx, setScreen, showToast }) {
  const { listing, event } = target;
  const { operators, riders, setBookings, RIDER_ID } = ctx;
  const op = operators.find(o=>o.id===listing.operatorId);
  const driver = op?.drivers.find(d=>d.id===listing.driverId);
  const vehicle = op?.vehicles.find(v=>v.id===listing.vehicleId);
  const rider = riders.find(r=>r.id===RIDER_ID);

  const [step, setStep] = useState(0); // 0=review 1=details 2=confirm 3=done
  const [seats, setSeats] = useState(1);
  const [name, setName] = useState(rider?.name||"");
  const [email, setEmail] = useState(rider?.email||"");
  const [phone, setPhone] = useState(rider?.phone||"");
  const [useCard, setUseCard] = useState(rider?.cards?.[0]?.id||null);
  const [errs, setErrs] = useState({});
  const [bookingRef, setBookingRef] = useState(null);

  const total = listing.price * seats;
  const primaryCard = rider?.cards?.find(c=>c.id===useCard);

  function confirmBooking() {
    const bk = {
      id:"b"+Date.now(), listingId:listing.id, riderId:RIDER_ID,
      riderName:name, riderPhone:phone, riderEmail:email,
      seats, total, status:"pending_confirmation",
      created:new Date().toISOString(), expiresAt:new Date(Date.now()+24*3600*1000).toISOString(),
      paymentStatus:"held",
    };
    setBookings(prev=>[...prev, bk]);
    setBookingRef(bk.id);
    setStep(3);
    showToast("Booking request sent!");
  }

  if (step===3) return (
    <div style={S.page}>
      <div style={S.confirmWrap}>
        <div style={{ textAlign:"center", marginBottom:20 }}>
          <span style={{ fontSize:56 }}>⏳</span>
          <h2 style={{ ...S.bigTitle, color:"#fbbf24", marginTop:8 }}>AWAITING CONFIRMATION</h2>
          <p style={{ color:"#666", fontSize:14, marginTop:6 }}>R{total} held securely in escrow</p>
        </div>
        <div style={S.confirmBox}>
          {[["Ref", bookingRef?.toUpperCase()],["Event",event.name],["Operator",op?.name],["From",listing.location],["Date",listing.date+" · "+listing.time],["Seats",seats],["Total","R"+total.toLocaleString()]].map(([k,v],i)=>(
            <div key={i} style={{ ...S.cRow, ...(k==="Total"?{borderTop:`1px solid ${event.color}33`,paddingTop:10,marginTop:4}:{}) }}>
              <span style={S.cLbl}>{k}</span>
              <span style={{ ...S.cVal, ...(k==="Total"?{color:event.color,fontWeight:700,fontSize:18}:{}) }}>{v}</span>
            </div>
          ))}
        </div>
        <Notice>Driver has 24 hours to confirm. If no response you will be automatically refunded in full.</Notice>
        <button style={{ ...S.btnPrimary, width:"100%", marginTop:16 }} onClick={()=>setScreen("event")}>← Back to shuttles</button>
      </div>
    </div>
  );

  return (
    <div style={S.page}>
      <button onClick={()=>setScreen("event")} style={S.backBtn}>← Back to shuttles</button>
      <StepBar steps={["Review","Details","Confirm"]} current={step} />

      {step===0 && (
        <div style={S.bookCard}>
          <SHead title="Trip Details" sub="Confirm before booking" />
          {/* Event banner */}
          <div style={{ ...S.bookEventBanner, borderLeft:`4px solid ${event.color}` }}>
            <span style={{ fontSize:28 }}>{event.banner}</span>
            <div>
              <div style={{ fontWeight:700 }}>{event.name}</div>
              <div style={{ color:"#666", fontSize:13 }}>{listing.date} · {listing.time} · {listing.direction==="to"?"→ To Event":"← From Event"}</div>
            </div>
          </div>
          {/* Operator */}
          <div style={{ display:"flex", gap:12, alignItems:"center", margin:"14px 0" }}>
            <span style={{ fontSize:28 }}>{op?.logo}</span>
            <div style={{ flex:1 }}>
              <div style={{ fontWeight:700 }}>{op?.name} <StatusBadge status={op?.status} small /></div>
              <div style={{ color:"#f0a030", fontSize:12 }}>{stars(op?.rating)} {op?.rating}</div>
            </div>
            <div style={{ textAlign:"right" }}>
              <div style={{ color:event.color, fontFamily:"'Bebas Neue',sans-serif", fontSize:30 }}>R{listing.price}</div>
              <div style={{ color:"#555", fontSize:11 }}>per person</div>
            </div>
          </div>
          {/* Driver */}
          {driver && (
            <div style={S.trustCard}>
              <p style={S.trustMicroTitle}>ASSIGNED DRIVER</p>
              <div style={S.driverRow}>
                <div style={S.driverAvatar}>{driver.photo}</div>
                <div><div style={{ fontWeight:600 }}>{driver.name}</div><div style={{ color:"#666", fontSize:12 }}>PDP: {driver.pdp} · {driver.phone}</div></div>
                <StatusBadge status={driver.status} small />
              </div>
              {vehicle && <>
                <p style={{ ...S.trustMicroTitle, marginTop:12 }}>VEHICLE</p>
                <div style={S.driverRow}>
                  <span style={{ fontSize:24 }}>🚐</span>
                  <div><div style={{ fontWeight:600 }}>{vehicle.make} · {vehicle.colour}</div><div style={{ color:"#666", fontSize:12 }}>🪪 {vehicle.plate} · {vehicle.seats} seats</div></div>
                  <StatusBadge status={vehicle.status} small />
                </div>
              </>}
              {listing.amenities?.length>0 && (
                <div style={{ ...S.amenityRow, marginTop:12 }}>
                  {listing.amenities.map(a=><span key={a} style={S.amenityChip}>{AMENITY_ICONS[a]} {a.toUpperCase()}</span>)}
                </div>
              )}
            </div>
          )}
          <button style={{ ...S.btnPrimary, background:event.color, width:"100%", marginTop:16 }} onClick={()=>setStep(1)}>Continue →</button>
        </div>
      )}

      {step===1 && (
        <div style={S.bookCard}>
          <SHead title="Your Details" sub="Who is travelling?" />
          <FormF label="Full Name" val={name} set={setName} ph="Your full name" err={errs.name} />
          <FormF label="Email" val={email} set={setEmail} ph="you@email.com" type="email" err={errs.email} />
          <FormF label="Phone / WhatsApp" val={phone} set={setPhone} ph="+27 82 000 0000" type="tel" err={errs.phone} />
          <div style={{ marginBottom:16 }}>
            <label style={S.formLbl}>Seats</label>
            <div style={{ display:"flex", gap:12, alignItems:"center", marginTop:6 }}>
              <button style={S.cntBtn} onClick={()=>setSeats(s=>Math.max(1,s-1))}>−</button>
              <span style={{ fontWeight:700, fontSize:22, minWidth:28, textAlign:"center" }}>{seats}</span>
              <button style={S.cntBtn} onClick={()=>setSeats(s=>Math.min(listing.seatsLeft,s+1))}>+</button>
              <span style={{ color:"#555", fontSize:13 }}>{listing.seatsLeft} available</span>
            </div>
          </div>
          {/* Card selection */}
          {rider?.cards?.length>0 && (
            <div style={{ marginBottom:16 }}>
              <label style={S.formLbl}>Pay With</label>
              {rider.cards.map(c=>(
                <div key={c.id} onClick={()=>setUseCard(c.id)} style={{ ...S.cardSelectRow, ...(useCard===c.id?{borderColor:"#c8f04a44",background:"#0f160a"}:{}) }}>
                  <span style={{ fontSize:20 }}>💳</span>
                  <span style={{ flex:1, fontSize:13 }}>•••• {c.last4} · {c.expiry}</span>
                  {useCard===c.id && <span style={{ color:"#c8f04a", fontSize:13 }}>✓</span>}
                </div>
              ))}
            </div>
          )}
          <div style={{ ...S.totalBar, borderColor:event.color+"44" }}>
            <span style={{ color:"#666" }}>{seats} × R{listing.price}</span>
            <span style={{ ...S.totalAmt, color:event.color }}>R{total.toLocaleString()}</span>
          </div>
          <Notice>💳 Payment held in escrow until driver confirms within 24h. Auto-refund if no response.</Notice>
          <div style={{ display:"flex", gap:10, marginTop:16 }}>
            <button style={S.btnSecondary} onClick={()=>setStep(0)}>← Back</button>
            <button style={{ ...S.btnPrimary, background:event.color, flex:1 }} onClick={()=>{
              const e={};
              if(!name.trim())e.name="Required";
              if(!email.includes("@"))e.email="Valid email required";
              if(phone.replace(/\D/g,"").length<9)e.phone="Required";
              setErrs(e); if(!Object.keys(e).length)setStep(2);
            }}>Review →</button>
          </div>
        </div>
      )}

      {step===2 && (
        <div style={S.bookCard}>
          <SHead title="Confirm Booking" sub="Final check before payment" />
          <div style={S.confirmBox}>
            {[["Event",event.name],["Route",listing.location+" "+(listing.direction==="to"?"→":"←")+" "+event.name],["Date",listing.date+" · "+listing.time],["Operator",op?.name],["Passenger",name],["Phone",phone],["Seats",seats],["Payment",primaryCard?"•••• "+primaryCard.last4:"At confirmation"]].map(([k,v],i)=>(
              <div key={i} style={S.cRow}><span style={S.cLbl}>{k}</span><span style={S.cVal}>{v}</span></div>
            ))}
            <div style={{ ...S.cRow, borderTop:`1px solid ${event.color}33`, paddingTop:10, marginTop:4 }}>
              <span style={S.cLbl}>Total</span>
              <span style={{ color:event.color, fontWeight:700, fontSize:20 }}>R{total.toLocaleString()}</span>
            </div>
          </div>
          <div style={{ display:"flex", gap:10, marginTop:16 }}>
            <button style={S.btnSecondary} onClick={()=>setStep(1)}>← Back</button>
            <button style={{ ...S.btnPrimary, background:event.color, flex:1 }} onClick={confirmBooking}>Confirm & Pay →</button>
          </div>
        </div>
      )}
    </div>
  );
}

// ─── ACCOUNT SCREEN ───────────────────────────────────────────────────────────
function AccountScreen({ ctx, setScreen, showToast }) {
  const { riders, setRiders, bookings, reviews, setReviews, RIDER_ID, operators, listings, events } = ctx;
  const rider = riders.find(r=>r.id===RIDER_ID);
  const [tab, setTab] = useState("profile");
  const [saved, setSaved] = useState(false);
  const [name, setName] = useState(rider?.name||"");
  const [email, setEmail] = useState(rider?.email||"");
  const [phone, setPhone] = useState(rider?.phone||"");
  const [notifs, setNotifs] = useState(rider?.notifications||{bookingUpdates:true,promos:false,reminders:true});
  const [selfieUpdated, setSelfieUpdated] = useState(false);
  const [cards, setCards] = useState(rider?.cards||[]);
  const [showAddCard, setShowAddCard] = useState(false);
  const [cardForm, setCardForm] = useState({number:"",name:"",expiry:"",cvv:""});
  const [cardErrs, setCardErrs] = useState({});
  const [reviewDraft, setReviewDraft] = useState({});
  const [reviewStars, setReviewStars] = useState({});

  const myBookings = bookings.filter(b=>b.riderId===RIDER_ID);
  const completedBookings = myBookings.filter(b=>b.status==="confirmed"||b.status==="completed");

  function saveProfile() {
    setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,name,email,phone,notifications:notifs}));
    setSaved(true); setTimeout(()=>setSaved(false),2000);
    showToast("Profile saved!");
  }

  function addCard() {
    const e={};
    if(cardForm.number.replace(/\s/g,"").length<13)e.number="Valid card number required";
    if(!cardForm.name.trim())e.name="Name required";
    if(cardForm.expiry.length<5)e.expiry="Valid expiry required";
    if(cardForm.cvv.replace(/\D/g,"").length<3)e.cvv="CVV required";
    setCardErrs(e); if(Object.keys(e).length)return;
    const type=detectCardType(cardForm.number);
    const last4=cardForm.number.replace(/\s/g,"").slice(-4);
    const nc={ id:"c"+Date.now(), type, last4, expiry:cardForm.expiry, name:cardForm.name.toUpperCase(), primary:cards.length===0 };
    const updated=[...cards,nc];
    setCards(updated);
    setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,cards:updated}));
    setCardForm({number:"",name:"",expiry:"",cvv:""}); setShowAddCard(false);
    showToast("Card added!");
  }

  function setPrimary(id) {
    const u=cards.map(c=>({...c,primary:c.id===id}));
    setCards(u); setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,cards:u}));
  }

  function removeCard(id) {
    const u=cards.filter(c=>c.id!==id).map((c,i)=>({...c,primary:i===0}));
    setCards(u); setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,cards:u}));
    showToast("Card removed");
  }

  function submitReview(bookingId, operatorId) {
    const rating=reviewStars[bookingId]||5;
    const comment=reviewDraft[bookingId]||"";
    if(!comment.trim()){showToast("Please write a review","error");return;}
    setReviews(prev=>[...prev,{id:"rv"+Date.now(),operatorId,riderId:RIDER_ID,riderName:rider.name,rating,comment,date:new Date().toLocaleDateString("en-ZA"),bookingId}]);
    setReviewDraft(p=>({...p,[bookingId]:""}));
    showToast("Review submitted! ⭐");
  }

  const VER_STEPS=[
    {label:"Personal Details",desc:"Name, email, phone, SA ID number",done:true},
    {label:"ID Document",desc:"Green ID book or Smart ID card",done:rider?.status!=="unverified"},
    {label:"Selfie Photo",desc:"Face photo matching ID",done:rider?.status!=="unverified"},
    {label:"Admin Review",desc:"Manual identity check by Shuttlr team",done:rider?.status==="verified"},
  ];

  if(!rider) return <div style={S.page}><Empty icon="👤" msg="No account found. Please register." /></div>;

  return (
    <div style={S.page}>
      {/* Header */}
      <div style={S.acctHeader}>
        <div style={S.acctAvatarWrap}>
          <div style={S.acctAvatar}><span style={{fontSize:40}}>{rider.selfie}</span></div>
          <div style={S.acctAvatarBadge}><StatusBadge status={rider.status} small /></div>
        </div>
        <div style={{flex:1}}>
          <h2 style={S.acctName}>{rider.name}</h2>
          <p style={{color:"#555",fontSize:13}}>{rider.email}</p>
          <div style={{display:"flex",gap:12,marginTop:6,flexWrap:"wrap"}}>
            <span style={S.acctStat}><strong style={{color:"#c8f04a"}}>{rider.bookings}</strong> trips</span>
            <span style={S.acctStat}><strong style={{color:"#c8f04a"}}>{cards.length}</strong> card{cards.length!==1?"s":""}</span>
            <span style={S.acctStat}><strong style={{color:rider.status==="verified"?"#4ade80":"#fbbf24"}}>{STATUS_LABELS[rider.status]}</strong></span>
          </div>
        </div>
      </div>

      {/* Tabs */}
      <div style={S.dashTabs}>
        {[["profile","👤 Profile"],["verification","🪪 Verification"],["payment","💳 Payment"],["bookings","📋 Bookings"],["reviews","⭐ Reviews"],["notifications","🔔 Alerts"]].map(([t,l])=>(
          <button key={t} onClick={()=>setTab(t)} style={{...S.dashTab,...(tab===t?S.dashTabActive:{})}}>{l}</button>
        ))}
      </div>

      {/* ── PROFILE ── */}
      {tab==="profile" && (
        <div style={S.settCard}>
          <SHead title="Edit Profile" sub="Visible to drivers when you book" />
          {saved && <FlashMsg>✓ Profile saved</FlashMsg>}
          <div style={S.selfieRow}>
            <div style={S.selfieCircle}><span style={{fontSize:44}}>{rider.selfie}</span>{selfieUpdated&&<div style={S.selfieCheck}>✓</div>}</div>
            <div style={{flex:1}}>
              <p style={{fontSize:13,color:"#666",marginBottom:8,lineHeight:1.6}}>Profile photo is verified. Updating triggers re-verification.</p>
              <UploadBox label="Update Selfie" uploaded={selfieUpdated} onUpload={()=>setSelfieUpdated(true)} icon="🤳" hint="New selfie — requires re-verification" camera />
            </div>
          </div>
          <div style={{height:1,background:"#14141e",margin:"20px 0"}} />
          <FormF label="Full Name" val={name} set={setName} ph="Your full name" />
          <FormF label="Email Address" val={email} set={setEmail} ph="you@email.com" type="email" />
          <FormF label="Phone / WhatsApp" val={phone} set={setPhone} ph="+27 82 000 0000" type="tel" />
          <div style={{marginBottom:16}}>
            <label style={S.formLbl}>SA ID Number</label>
            <div style={S.idLocked}>{rider.id_number} <span style={{color:"#444",fontSize:11}}>🔒 Cannot be changed</span></div>
          </div>
          <div style={{height:1,background:"#14141e",margin:"20px 0"}} />
          <div style={S.dangerZone}>
            <p style={{fontSize:10,color:"#555",letterSpacing:2,textTransform:"uppercase",marginBottom:10}}>DANGER ZONE</p>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",gap:12}}>
              <div>
                <div style={{fontSize:14,fontWeight:600,color:"#f87171"}}>Delete Account</div>
                <div style={{fontSize:12,color:"#555",marginTop:2}}>Permanently removes your data. Active bookings will be cancelled.</div>
              </div>
              <button style={S.btnDanger} onClick={()=>showToast("Account deletion requires email confirmation","warn")}>Delete</button>
            </div>
          </div>
          <button style={{...S.btnPrimary,marginTop:20}} onClick={saveProfile}>Save Changes</button>
        </div>
      )}

      {/* ── VERIFICATION ── */}
      {tab==="verification" && (
        <div style={S.settCard}>
          <SHead title="Identity Verification" />
          <div style={{...S.verBanner,background:rider.status==="verified"?"#0d1f0d":"#1a1200",borderColor:rider.status==="verified"?"#4ade8033":"#fbbf2433"}}>
            <span style={{fontSize:32}}>{rider.status==="verified"?"✅":rider.status==="id_submitted"?"⏳":"⚠️"}</span>
            <div>
              <div style={{fontWeight:700,fontSize:16,color:rider.status==="verified"?"#4ade80":"#fbbf24"}}>
                {rider.status==="verified"?"Identity Verified":rider.status==="id_submitted"?"Verification Pending":"Not Yet Verified"}
              </div>
              <div style={{fontSize:13,color:"#666",marginTop:3}}>
                {rider.status==="verified"?"Your identity is confirmed. Drivers see your verified badge.":rider.status==="id_submitted"?"Your documents are under review (2–4 hours).":"Verify your ID to unlock full booking features."}
              </div>
            </div>
          </div>
          <div style={{marginTop:24,marginBottom:24}}>
            {VER_STEPS.map((st,i)=>(
              <div key={st.label} style={{display:"flex",gap:14,alignItems:"flex-start",marginBottom:18,position:"relative"}}>
                <div style={{...S.verDot,background:st.done?"#4ade80":"#1a1a24",borderColor:st.done?"#4ade80":"#2a2a3a",color:st.done?"#000":"#555"}}>{st.done?"✓":i+1}</div>
                {i<VER_STEPS.length-1&&<div style={{position:"absolute",left:13,top:28,width:2,height:"calc(100% + 4px)",background:st.done?"#4ade8033":"#1a1a24"}} />}
                <div style={{flex:1}}>
                  <div style={{fontWeight:600,fontSize:14,color:st.done?"#ddd":"#666"}}>{st.label}</div>
                  <div style={{fontSize:12,color:"#555",marginTop:2}}>{st.desc}</div>
                </div>
                <span style={{fontSize:12,color:st.done?"#4ade80":"#555"}}>{st.done?"Done":"Pending"}</span>
              </div>
            ))}
          </div>
          <SHead title="What Drivers See" sub="" />
          <div style={{display:"flex",gap:14,alignItems:"center",background:"#12121a",border:"1px solid #1e1e2a",borderRadius:10,padding:"14px 16px",marginBottom:12}}>
            <div style={{width:48,height:48,background:"#1a1a28",borderRadius:"50%",display:"flex",alignItems:"center",justifyContent:"center",fontSize:26}}>{rider.selfie}</div>
            <div>
              <div style={{fontWeight:700,fontSize:15}}>{rider.name}</div>
              <div style={{color:"#666",fontSize:13,marginTop:2,display:"flex",gap:8,alignItems:"center"}}>{rider.bookings} trips · <StatusBadge status={rider.status} small /></div>
            </div>
          </div>
          <Notice>Drivers never see your ID number. Only name, photo, trip count and verification badge are visible.</Notice>
          {rider.status!=="verified"&&<button style={{...S.btnPrimary,marginTop:16,width:"100%"}} onClick={()=>setScreen("verify")}>Complete Verification →</button>}
        </div>
      )}

      {/* ── PAYMENT ── */}
      {tab==="payment" && (
        <div style={S.settCard}>
          <SHead title="Payment Methods" sub="Secured and tokenised via Peach Payments" />
          <Notice>💳 Shuttlr never stores your full card number. All transactions use tokenised secure processing.</Notice>
          {cards.length===0
            ? <Empty icon="💳" msg="No saved cards yet." />
            : cards.map(c=>(
              <div key={c.id} className="card-hover" style={{...S.cardRow,...(c.primary?{borderColor:"#c8f04a44",background:"#0f160a"}:{})}}>
                <div style={S.cardVisual}>
                  <div style={S.cardChip} />
                  <div style={{fontSize:11,color:"#666",textTransform:"uppercase",letterSpacing:2,marginBottom:6}}>{c.type}</div>
                  <div style={{fontFamily:"monospace",fontSize:15,letterSpacing:3,color:"#ddd",marginBottom:8}}>•••• •••• •••• {c.last4}</div>
                  <div style={{display:"flex",justifyContent:"space-between",fontSize:12,color:"#888",fontFamily:"monospace"}}><span>{c.name}</span><span>{c.expiry}</span></div>
                </div>
                <div style={{display:"flex",flexDirection:"column",gap:6,alignItems:"flex-end"}}>
                  {c.primary?<span style={S.primaryBadge}>★ Primary</span>:<button style={S.setDefBtn} onClick={()=>setPrimary(c.id)}>Set primary</button>}
                  <button style={S.removeCardBtn} onClick={()=>removeCard(c.id)}>✕ Remove</button>
                </div>
              </div>
            ))
          }
          {!showAddCard
            ? <button style={{...S.btnSecondary,width:"100%",marginTop:8}} onClick={()=>setShowAddCard(true)}>+ Add New Card</button>
            : <div style={S.addCardWrap}>
                <p style={S.addSubTitle}>ADD NEW CARD</p>
                <div style={{position:"relative",marginBottom:14}}>
                  <label style={S.formLbl}>Card Number</label>
                  <input style={{...S.inp,paddingRight:44,...(cardErrs.number?{borderColor:"#f87171"}:{})}} value={cardForm.number} onChange={e=>setCardForm(p=>({...p,number:formatCardNum(e.target.value)}))} placeholder="1234 5678 9012 3456" maxLength={19} />
                  <span style={{position:"absolute",right:12,bottom:10,fontSize:20}}>{cardForm.number?detectCardType(cardForm.number)==="visa"?"💙":detectCardType(cardForm.number)==="mastercard"?"🔴":"💳":"💳"}</span>
                  {cardErrs.number&&<ErrTxt>{cardErrs.number}</ErrTxt>}
                </div>
                <FormF label="Cardholder Name" val={cardForm.name} set={v=>setCardForm(p=>({...p,name:v}))} ph="As printed on card" err={cardErrs.name} />
                <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:14}}>
                  <div>
                    <label style={S.formLbl}>Expiry</label>
                    <input style={{...S.inp,...(cardErrs.expiry?{borderColor:"#f87171"}:{})}} value={cardForm.expiry} onChange={e=>setCardForm(p=>({...p,expiry:formatExpiry(e.target.value)}))} placeholder="MM/YY" maxLength={5} />
                    {cardErrs.expiry&&<ErrTxt>{cardErrs.expiry}</ErrTxt>}
                  </div>
                  <div>
                    <label style={S.formLbl}>CVV</label>
                    <input style={{...S.inp,...(cardErrs.cvv?{borderColor:"#f87171"}:{})}} value={cardForm.cvv} onChange={e=>setCardForm(p=>({...p,cvv:e.target.value.replace(/\D/g,"").slice(0,4)}))} placeholder="•••" type="password" maxLength={4} />
                    {cardErrs.cvv&&<ErrTxt>{cardErrs.cvv}</ErrTxt>}
                  </div>
                </div>
                <div style={{display:"flex",gap:10,marginTop:14}}>
                  <button style={S.btnSecondary} onClick={()=>{setShowAddCard(false);setCardErrs({});}}>Cancel</button>
                  <button style={{...S.btnPrimary,flex:1}} onClick={addCard}>🔒 Save Card Securely</button>
                </div>
              </div>
          }
          {myBookings.length>0&&<>
            <div style={{height:1,background:"#14141e",margin:"24px 0"}} />
            <SHead title="Billing History" sub="" />
            {myBookings.map(b=>(
              <div key={b.id} style={{display:"flex",justifyContent:"space-between",padding:"11px 0",borderBottom:"1px solid #14141e"}}>
                <div><div style={{fontSize:14,fontWeight:500}}>Booking {b.id.toUpperCase()}</div><div style={{fontSize:12,color:"#555",marginTop:2}}>{b.seats} seat{b.seats!==1?"s":""}</div></div>
                <div style={{textAlign:"right"}}>
                  <div style={{fontWeight:700,color:"#c8f04a"}}>R{b.total}</div>
                  <div style={{fontSize:12,color:b.paymentStatus==="refunded"?"#f87171":b.paymentStatus==="released"?"#4ade80":"#fbbf24",marginTop:2}}>
                    {b.paymentStatus==="refunded"?"↩ Refunded":b.paymentStatus==="released"?"✓ Paid":"⏳ Held"}
                  </div>
                </div>
              </div>
            ))}
          </>}
        </div>
      )}

      {/* ── BOOKINGS ── */}
      {tab==="bookings" && (
        <div style={S.settCard}>
          <SHead title="My Bookings" />
          {myBookings.length===0
            ? <Empty icon="🎫" msg="No bookings yet." />
            : myBookings.map(b=>{
                const bs=BOOKING_STATUS[b.status];
                const listing=ctx.listings.find(l=>l.id===b.listingId);
                const event=ctx.events.find(e=>e.id===listing?.eventId);
                return(
                  <div key={b.id} style={{...S.bookingCard,borderLeft:`3px solid ${bs.color}`}}>
                    <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
                      <div>
                        {event&&<div style={{fontSize:11,color:event.color,textTransform:"uppercase",letterSpacing:1,marginBottom:4}}>{event.name}</div>}
                        <div style={{fontWeight:600}}>{listing?.location} {listing?.direction==="to"?"→ Event":"← Event"}</div>
                        <div style={{color:"#666",fontSize:13,marginTop:2}}>{listing?.date} · {listing?.time} · {b.seats} seat{b.seats!==1?"s":""}</div>
                        <div style={{color:"#555",fontSize:12,marginTop:2}}>{new Date(b.created).toLocaleDateString("en-ZA")}</div>
                      </div>
                      <div style={{textAlign:"right"}}>
                        <div style={{fontWeight:700,color:"#c8f04a",fontSize:16}}>R{b.total}</div>
                        <span style={{...S.statusChip,background:bs.color+"22",color:bs.color}}>{bs.label}</span>
                      </div>
                    </div>
                  </div>
                );
              })
          }
        </div>
      )}

      {/* ── REVIEWS ── */}
      {tab==="reviews" && (
        <div style={S.settCard}>
          <SHead title="Reviews" sub="Rate your completed trips" />
          {completedBookings.length===0
            ? <Empty icon="⭐" msg="Complete a trip to leave a review." />
            : completedBookings.map(b=>{
                const listing=ctx.listings.find(l=>l.id===b.listingId);
                const op=ctx.operators.find(o=>o.id===listing?.operatorId);
                const alreadyReviewed=reviews.find(r=>r.bookingId===b.id&&r.riderId===RIDER_ID);
                if(!op)return null;
                return(
                  <div key={b.id} style={{...S.reviewWrap,marginBottom:16}}>
                    <div style={{display:"flex",gap:10,alignItems:"center",marginBottom:12}}>
                      <span style={{fontSize:24}}>{op.logo}</span>
                      <div style={{flex:1}}>
                        <div style={{fontWeight:600}}>{op.name}</div>
                        <div style={{color:"#666",fontSize:12}}>Booking {b.id.toUpperCase()} · {listing?.date}</div>
                      </div>
                      {alreadyReviewed&&<span style={{color:"#4ade80",fontSize:12}}>✓ Reviewed</span>}
                    </div>
                    {alreadyReviewed
                      ? <div style={{background:"#0d1f0d",border:"1px solid #4ade8033",borderRadius:8,padding:"10px 14px"}}>
                          <div style={{color:"#f0a030",marginBottom:4}}>{stars(alreadyReviewed.rating)}</div>
                          <div style={{fontSize:13,color:"#aaa"}}>{alreadyReviewed.comment}</div>
                        </div>
                      : <>
                          <div style={{display:"flex",gap:6,marginBottom:10}}>
                            {[1,2,3,4,5].map(n=>(
                              <button key={n} onClick={()=>setReviewStars(p=>({...p,[b.id]:n}))}
                                style={{fontSize:22,background:"none",border:"none",cursor:"pointer",color:(reviewStars[b.id]||0)>=n?"#f0a030":"#333"}}>★</button>
                            ))}
                            <span style={{color:"#555",fontSize:13,alignSelf:"center"}}>{reviewStars[b.id]||0}/5</span>
                          </div>
                          <textarea value={reviewDraft[b.id]||""} onChange={e=>setReviewDraft(p=>({...p,[b.id]:e.target.value}))}
                            placeholder="How was your ride? (required)" rows={3}
                            style={{...S.inp,resize:"none",marginBottom:10}} />
                          <button style={{...S.btnPrimary,fontSize:13,padding:"8px 18px"}} onClick={()=>submitReview(b.id,op.id)}>Submit Review</button>
                        </>
                    }
                  </div>
                );
              })
          }
          {reviews.filter(r=>r.riderId===RIDER_ID).length>0&&<>
            <SHead title="Your Past Reviews" sub="" />
            {reviews.filter(r=>r.riderId===RIDER_ID).map(r=><ReviewCard key={r.id} review={r} />)}
          </>}
        </div>
      )}

      {/* ── NOTIFICATIONS ── */}
      {tab==="notifications" && (
        <div style={S.settCard}>
          <SHead title="Notification Preferences" sub="Control what alerts you receive" />
          {[
            {key:"bookingUpdates",label:"Booking Updates",desc:"Confirmation, declines, payment status changes"},
            {key:"reminders",label:"Trip Reminders",desc:"Reminder 24h and 2h before your shuttle departs"},
            {key:"promos",label:"Promotions & New Events",desc:"New events, early bird deals and operator offers"},
          ].map(({key,label,desc})=>(
            <div key={key} className="set-row" style={S.notifRow} onClick={()=>setNotifs(p=>({...p,[key]:!p[key]}))}>
              <div style={{flex:1}}>
                <div style={{fontWeight:600,fontSize:14}}>{label}</div>
                <div style={{color:"#555",fontSize:12,marginTop:2}}>{desc}</div>
              </div>
              <div style={{...S.toggle,background:notifs[key]?"#c8f04a":"#2a2a3a"}}>
                <div style={{...S.toggleThumb,transform:notifs[key]?"translateX(20px)":"translateX(2px)"}} />
              </div>
            </div>
          ))}
          <div style={{height:1,background:"#14141e",margin:"20px 0"}} />
          <SHead title="Contact Preferences" sub="" />
          <Notice>For critical booking updates, we always contact you via WhatsApp on {rider.phone} regardless of settings above.</Notice>
          <button style={{...S.btnPrimary,marginTop:16}} onClick={()=>{setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,notifications:notifs}));showToast("Preferences saved!");}}>Save Preferences</button>
        </div>
      )}
    </div>
  );
}

// ─── VERIFY RIDER SCREEN ──────────────────────────────────────────────────────
function VerifyRiderScreen({ ctx, setScreen, showToast }) {
  const { riders, setRiders, RIDER_ID } = ctx;
  const [step, setStep] = useState(0);
  const [form, setForm] = useState({name:"",email:"",phone:"",id_number:""});
  const [idUploaded, setIdUploaded] = useState(false);
  const [selfieUploaded, setSelfieUploaded] = useState(false);
  const [errs, setErrs] = useState({});

  function next() {
    if(step===0){
      const e={};
      if(!form.name.trim())e.name="Required";
      if(!form.email.includes("@"))e.email="Valid email required";
      if(form.phone.replace(/\D/g,"").length<9)e.phone="Required";
      if(form.id_number.replace(/\D/g,"").length<13)e.id_number="Must be 13 digits";
      setErrs(e); if(Object.keys(e).length)return;
    }
    setStep(s=>s+1);
  }

  function finish() {
    setRiders(prev=>prev.map(r=>r.id!==RIDER_ID?r:{...r,...form,status:"id_submitted"}));
    setStep(3); showToast("Verification submitted!");
  }

  return (
    <div style={S.page}>
      <button onClick={()=>setScreen("account")} style={S.backBtn}>← Back</button>
      <SHead title="Verify Your Identity" sub="Required to book on Shuttlr" />
      <StepBar steps={["Details","ID Upload","Selfie","Done"]} current={step} />
      <div style={S.formPanel}>
        {step===0&&<>
          <Notice>Your ID is only seen by Shuttlr admin. It is never shared with operators or drivers.</Notice>
          <FormF label="Full Name" val={form.name} set={v=>setForm(p=>({...p,name:v}))} ph="As on your ID" err={errs.name} />
          <FormF label="Email" val={form.email} set={v=>setForm(p=>({...p,email:v}))} ph="you@email.com" type="email" err={errs.email} />
          <FormF label="Phone / WhatsApp" val={form.phone} set={v=>setForm(p=>({...p,phone:v}))} ph="+27 82 000 0000" type="tel" err={errs.phone} />
          <FormF label="SA ID Number" val={form.id_number} set={v=>setForm(p=>({...p,id_number:v}))} ph="13-digit ID" err={errs.id_number} />
          <button style={S.btnPrimary} onClick={next}>Next →</button>
        </>}
        {step===1&&<>
          <Notice>Upload a clear, unobstructed photo of your green ID book (photo page open) or Smart ID card (front).</Notice>
          <UploadBox label="SA ID Document" uploaded={idUploaded} onUpload={()=>setIdUploaded(true)} icon="🪪" hint="Green ID book or Smart ID (front)" />
          <div style={{display:"flex",gap:10,marginTop:20}}>
            <button style={S.btnSecondary} onClick={()=>setStep(0)}>← Back</button>
            <button style={{...S.btnPrimary,flex:1,...(!idUploaded?{opacity:.4,cursor:"not-allowed"}:{})}} onClick={()=>idUploaded&&next()}>Next →</button>
          </div>
        </>}
        {step===2&&<>
          <Notice>Take a clear selfie in good lighting. This becomes your profile photo visible to drivers. Must match your ID.</Notice>
          <UploadBox label="Selfie Photo" uploaded={selfieUploaded} onUpload={()=>setSelfieUploaded(true)} icon="🤳" hint="Clear face photo, good lighting" camera />
          <div style={{display:"flex",gap:10,marginTop:20}}>
            <button style={S.btnSecondary} onClick={()=>setStep(1)}>← Back</button>
            <button style={{...S.btnPrimary,flex:1,...(!selfieUploaded?{opacity:.4,cursor:"not-allowed"}:{})}} onClick={()=>selfieUploaded&&finish()}>Submit →</button>
          </div>
        </>}
        {step===3&&(
          <div style={{textAlign:"center"}}>
            <span style={{fontSize:52}}>⏳</span>
            <h3 style={{...S.bigTitle,color:"#fbbf24",marginTop:8,marginBottom:8}}>SUBMITTED</h3>
            <p style={{color:"#666",fontSize:14,lineHeight:1.8,marginBottom:24}}>Under review — usually 2–4 hours.<br/>You'll be notified on {form.phone||"your number"}.</p>
            <button style={{...S.btnPrimary,width:"100%"}} onClick={()=>setScreen("account")}>← Back to Account</button>
          </div>
        )}
      </div>
    </div>
  );
}

// ─── OPERATOR SCREEN ──────────────────────────────────────────────────────────
function OperatorScreen({ ctx, setScreen, showToast }) {
  const { operators, listings, setListings, bookings, setBookings, events } = ctx;
  const [selId, setSelId] = useState(null);
  const [tab, setTab] = useState("bookings");
  const [newL, setNewL] = useState({location:"",direction:"to",eventId:"rtd2026",date:"",time:"",price:"",seatsTotal:"",driverId:"",vehicleId:"",amenities:[]});

  const op = operators.find(o=>o.id===selId);
  const opListings = listings.filter(l=>l.operatorId===selId);
  const opBookings = bookings.filter(b=>opListings.find(l=>l.id===b.listingId));

  function handleBooking(id, action) {
    setBookings(prev=>prev.map(b=>b.id!==id?b:{...b,
      status:action==="confirm"?"confirmed":"declined",
      paymentStatus:action==="confirm"?"released":"refunded"}));
    showToast(action==="confirm"?"Booking confirmed! Payment released.":"Booking declined. Rider refunded.", action==="confirm"?"success":"warn");
  }

  function addListing() {
    if(!newL.location||!newL.time||!newL.price||!newL.seatsTotal||!newL.driverId||!newL.vehicleId){showToast("Please fill all fields","error");return;}
    const ev=events.find(e=>e.id===newL.eventId);
    const l={...newL,id:"l"+Date.now(),operatorId:selId,seatsLeft:parseInt(newL.seatsTotal),price:parseInt(newL.price),seatsTotal:parseInt(newL.seatsTotal),event:ev?.name||"",eventColor:ev?.color||"#c8f04a"};
    setListings(prev=>[...prev,l]);
    setNewL({location:"",direction:"to",eventId:"rtd2026",date:"",time:"",price:"",seatsTotal:"",driverId:"",vehicleId:"",amenities:[]});
    showToast("Listing published!");
  }

  if(!selId) return (
    <div style={S.page}>
      <SHead title="Operator Portal" sub="Select your company or register a new one" />
      <div style={S.opGrid}>
        {operators.map(op=>(
          <div key={op.id} className="hovcard" style={S.opCard} onClick={()=>setSelId(op.id)}>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
              <span style={{fontSize:32}}>{op.logo}</span>
              <StatusBadge status={op.status} small />
            </div>
            <div style={{fontWeight:700,fontSize:16,marginTop:8}}>{op.name}</div>
            <div style={{color:"#555",fontSize:13,marginTop:4}}>{op.drivers.length} drivers · {op.vehicles.length} vehicles</div>
            <div style={{color:"#555",fontSize:13}}>Balance: <span style={{color:"#c8f04a"}}>R{op.balance?.toLocaleString()}</span></div>
            <div style={{color:"#f0a030",fontSize:12,marginTop:4}}>{stars(op.rating)} {op.rating} ({op.reviews})</div>
          </div>
        ))}
        <div className="hovcard" style={{...S.opCard,border:"1.5px dashed #2a2a3a",alignItems:"center",justifyContent:"center",display:"flex",flexDirection:"column",gap:8}} onClick={()=>setScreen("op_reg")}>
          <span style={{fontSize:32,color:"#555"}}>+</span>
          <span style={{color:"#555",fontSize:14}}>Register New Operator</span>
        </div>
      </div>
    </div>
  );

  return (
    <div style={S.page}>
      <button onClick={()=>setSelId(null)} style={S.backBtn}>← All Operators</button>
      <div style={{display:"flex",gap:14,alignItems:"flex-start",flexWrap:"wrap",marginBottom:24}}>
        <span style={{fontSize:40}}>{op.logo}</span>
        <div>
          <h2 style={{fontFamily:"'Bebas Neue',sans-serif",fontSize:30,letterSpacing:2}}>{op.name}</h2>
          <div style={{display:"flex",gap:8,alignItems:"center",flexWrap:"wrap",marginTop:4}}>
            <StatusBadge status={op.status} />
            <span style={{color:"#555",fontSize:13}}>Balance: <span style={{color:"#c8f04a",fontWeight:600}}>R{op.balance?.toLocaleString()}</span></span>
            <span style={{color:"#f0a030",fontSize:13}}>{stars(op.rating)} {op.rating}</span>
          </div>
        </div>
      </div>
      {op.status!=="verified"&&<Notice>⚠️ Account pending verification. Listings won't appear publicly until approved.</Notice>}

      <div style={S.dashTabs}>
        {[["bookings","📋 Bookings"],["listings","🚐 Listings"],["team","👥 Team"],["earnings","💰 Earnings"]].map(([t,l])=>(
          <button key={t} onClick={()=>setTab(t)} style={{...S.dashTab,...(tab===t?S.dashTabActive:{})}}>{l}</button>
        ))}
      </div>

      {tab==="bookings"&&(
        <div>
          <SHead title="Incoming Bookings" sub="24 hours to confirm or decline" />
          {opBookings.length===0?<Empty icon="📭" msg="No bookings yet." />:opBookings.map(b=>{
            const hl=hoursLeft(b.expiresAt);
            const listing=listings.find(l=>l.id===b.listingId);
            return(
              <div key={b.id} style={{...S.bookingCard,borderLeft:`3px solid ${BOOKING_STATUS[b.status].color}`}}>
                <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
                  <div>
                    <div style={{fontWeight:600,fontSize:15}}>{b.riderName}</div>
                    <div style={{color:"#666",fontSize:13}}>{b.riderPhone} · {b.seats} seat{b.seats!==1?"s":""}</div>
                    <div style={{color:"#666",fontSize:12,marginTop:2}}>{listing?.location} {listing?.direction==="to"?"→":"←"} Event · {listing?.date} {listing?.time}</div>
                  </div>
                  <div style={{textAlign:"right"}}>
                    <div style={{color:"#c8f04a",fontWeight:700,fontSize:18}}>R{b.total}</div>
                    <span style={{...S.statusChip,background:BOOKING_STATUS[b.status].color+"22",color:BOOKING_STATUS[b.status].color}}>{BOOKING_STATUS[b.status].label}</span>
                  </div>
                </div>
                {b.status==="pending_confirmation"&&(
                  <div style={{marginTop:10}}>
                    <div style={{fontSize:13,fontWeight:500,color:hl<=6?"#f87171":"#fbbf24"}}>⏱ {hl}h remaining · Auto-refund if no action</div>
                    <div style={{display:"flex",gap:8,marginTop:8}}>
                      <button style={{...S.btnDanger,flex:1}} onClick={()=>handleBooking(b.id,"decline")}>✗ Decline</button>
                      <button style={{...S.btnSuccess,flex:2}} onClick={()=>handleBooking(b.id,"confirm")}>✓ Confirm Booking</button>
                    </div>
                  </div>
                )}
                {b.status==="confirmed"&&<div style={{color:"#4ade80",fontSize:13,marginTop:8}}>✓ Confirmed · Payment released to balance</div>}
                {b.status==="declined"&&<div style={{color:"#f87171",fontSize:13,marginTop:8}}>✗ Declined · Passenger refunded</div>}
              </div>
            );
          })}
        </div>
      )}

      {tab==="listings"&&(
        <div>
          <SHead title="My Listings" />
          {opListings.map(l=>(
            <div key={l.id} style={{...S.adminRow,borderLeft:`3px solid ${l.eventColor||"#c8f04a"}`}}>
              <div>
                <div style={{fontWeight:600}}>📍 {l.location} {l.direction==="to"?"→ Event":"← Event"}</div>
                <div style={{color:"#666",fontSize:13}}>{l.event} · {l.date} · {l.time} · R{l.price}/pp · {l.seatsLeft}/{l.seatsTotal}</div>
                <div style={{color:"#555",fontSize:12,marginTop:2}}>Driver: {op.drivers.find(d=>d.id===l.driverId)?.name||"—"} · Vehicle: {op.vehicles.find(v=>v.id===l.vehicleId)?.plate||"—"}</div>
              </div>
              <button style={S.delBtn} onClick={()=>setListings(prev=>prev.filter(x=>x.id!==l.id))}>✕</button>
            </div>
          ))}
          {op.status==="verified"&&(
            <div style={S.addSubForm}>
              <p style={S.addSubTitle}>ADD LISTING</p>
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"0 14px"}}>
                <FormF label="Pick-up Location" val={newL.location} set={v=>setNewL(p=>({...p,location:v}))} ph="e.g. Cape Town Airport" />
                <SelF label="Direction" val={newL.direction} set={v=>setNewL(p=>({...p,direction:v}))}><option value="to">→ To Event</option><option value="from">← From Event</option></SelF>
                <SelF label="Event" val={newL.eventId} set={v=>setNewL(p=>({...p,eventId:v}))}>{events.map(e=><option key={e.id} value={e.id}>{e.banner} {e.name}</option>)}</SelF>
                <FormF label="Date" val={newL.date} set={v=>setNewL(p=>({...p,date:v}))} ph="e.g. 2 Oct 2026" />
                <FormF label="Time" val={newL.time} set={v=>setNewL(p=>({...p,time:v}))} ph="08:00" />
                <FormF label="Price (R)" val={newL.price} set={v=>setNewL(p=>({...p,price:v}))} ph="250" type="number" />
                <FormF label="Total Seats" val={newL.seatsTotal} set={v=>setNewL(p=>({...p,seatsTotal:v}))} ph="16" type="number" />
                <SelF label="Driver" val={newL.driverId} set={v=>setNewL(p=>({...p,driverId:v}))}><option value="">Select driver</option>{op.drivers.filter(d=>d.status==="verified").map(d=><option key={d.id} value={d.id}>{d.name}</option>)}</SelF>
                <SelF label="Vehicle" val={newL.vehicleId} set={v=>setNewL(p=>({...p,vehicleId:v}))}><option value="">Select vehicle</option>{op.vehicles.filter(v=>v.status==="verified").map(v=><option key={v.id} value={v.id}>{v.plate} – {v.make}</option>)}</SelF>
              </div>
              <div style={{marginBottom:12}}>
                <label style={S.formLbl}>Amenities</label>
                <div style={{display:"flex",gap:8,flexWrap:"wrap",marginTop:6}}>
                  {Object.entries(AMENITY_ICONS).map(([k,v])=>(
                    <button key={k} onClick={()=>setNewL(p=>({...p,amenities:p.amenities.includes(k)?p.amenities.filter(a=>a!==k):[...p.amenities,k]}))}
                      style={{...S.pill,...(newL.amenities.includes(k)?S.pillActive:{})}}>{v} {k.toUpperCase()}</button>
                  ))}
                </div>
              </div>
              <button style={S.btnPrimary} onClick={addListing}>+ Publish Listing</button>
            </div>
          )}
        </div>
      )}

      {tab==="team"&&(
        <div>
          <SHead title="Drivers" />{op.drivers.map(d=>(
            <div key={d.id} style={S.adminRow}>
              <div style={{display:"flex",gap:12,alignItems:"center"}}>
                <div style={S.driverAvatar}>{d.photo}</div>
                <div><div style={{fontWeight:600}}>{d.name}</div><div style={{color:"#666",fontSize:13}}>PDP: {d.pdp} · {d.phone}</div></div>
              </div><StatusBadge status={d.status} />
            </div>
          ))}
          <SHead title="Vehicles" />{op.vehicles.map(v=>(
            <div key={v.id} style={S.adminRow}>
              <div><div style={{fontWeight:600}}>🚐 {v.plate} · {v.make}</div><div style={{color:"#666",fontSize:13}}>{v.colour} · {v.seats} seats · Roadworthy {v.roadworthy}</div></div>
              <StatusBadge status={v.status} />
            </div>
          ))}
        </div>
      )}

      {tab==="earnings"&&(
        <div>
          <SHead title="Earnings" sub="Shuttlr deducts 10% commission per confirmed booking" />
          <div style={{display:"grid",gridTemplateColumns:"repeat(auto-fill,minmax(160px,1fr))",gap:10,marginBottom:24}}>
            {[{label:"Available",val:`R${op.balance?.toLocaleString()}`,color:"#c8f04a"},{label:"Pending",val:`R${opBookings.filter(b=>b.paymentStatus==="held").reduce((s,b)=>s+b.total,0).toLocaleString()}`,color:"#fbbf24"},{label:"Lifetime",val:`R${((op.balance||0)+2400).toLocaleString()}`,color:"#4ade80"},{label:"Commission (10%)",val:`R${Math.round((op.balance||0)*0.1112).toLocaleString()}`,color:"#f87171"}].map(s=>(
              <div key={s.label} style={S.statCard}>
                <div style={{color:"#555",fontSize:11,marginBottom:6}}>{s.label}</div>
                <div style={{color:s.color,fontFamily:"'Bebas Neue',sans-serif",fontSize:28}}>{s.val}</div>
              </div>
            ))}
          </div>
          <Notice>Withdrawals processed within 24–48h. Contact payments@shuttlr.co.za to register your bank account.</Notice>
        </div>
      )}
    </div>
  );
}

// ─── OPERATOR REGISTRATION ────────────────────────────────────────────────────
function OperatorRegScreen({ ctx, setScreen, showToast }) {
  const { setOperators } = ctx;
  const [step, setStep] = useState(0);
  const [form, setForm] = useState({name:"",email:"",phone:"",cipc:"",logo:"🚐",description:""});
  const [owner, setOwner] = useState({name:"",id_number:"",id_doc:false,selfie:false});
  const [docs, setDocs] = useState({cipc:false,pdp:false,roadworthy:false});
  const [drivers, setDrivers] = useState([]);
  const [dForm, setDForm] = useState({name:"",pdp:"",phone:"",photo:false});
  const [vehicles, setVehicles] = useState([]);
  const [vForm, setVForm] = useState({plate:"",make:"",seats:"",colour:"",roadworthy:"",doc:false});

  function submit() {
    const op={id:"op"+Date.now(),name:form.name,logo:form.logo,status:"pending",rating:0,reviews:0,description:form.description,
      owner:{name:owner.name,id_number:owner.id_number,phone:form.phone,email:form.email},
      docs:{cipc:docs.cipc?"submitted":"missing",pdp:docs.pdp?"submitted":"missing",roadworthy:docs.roadworthy?"submitted":"missing",id_copy:owner.id_doc?"submitted":"missing",selfie:owner.selfie?"submitted":"missing"},
      drivers,vehicles,whatsapp:form.phone,balance:0};
    setOperators(prev=>[...prev,op]);
    setStep(5); showToast("Application submitted!");
  }

  const steps=["Company","Owner ID","Documents","Drivers","Vehicles","Done"];

  return (
    <div style={S.page}>
      <button onClick={()=>setScreen("operator")} style={S.backBtn}>← Back</button>
      <SHead title="Register Your Shuttle Service" sub="All fields required for verification" />
      <StepBar steps={steps} current={step} />
      <div style={S.formPanel}>
        {step===0&&<><FormF label="Company Name" val={form.name} set={v=>setForm(p=>({...p,name:v}))} ph="e.g. Cape Roller Shuttles" /><FormF label="Business Email" val={form.email} set={v=>setForm(p=>({...p,email:v}))} ph="bookings@co.za" type="email" /><FormF label="WhatsApp" val={form.phone} set={v=>setForm(p=>({...p,phone:v}))} ph="+27 82…" type="tel" /><FormF label="CIPC Number" val={form.cipc} set={v=>setForm(p=>({...p,cipc:v}))} ph="2024/123456/07" /><FormF label="Description" val={form.description} set={v=>setForm(p=>({...p,description:v}))} ph="What makes your service great?" /><button style={S.btnPrimary} onClick={()=>form.name&&setStep(1)}>Next →</button></>}
        {step===1&&<><Notice>Owner ID reviewed only by Shuttlr admin. Never shared with public.</Notice><FormF label="Owner Full Name" val={owner.name} set={v=>setOwner(p=>({...p,name:v}))} ph="As on ID" /><FormF label="SA ID Number" val={owner.id_number} set={v=>setOwner(p=>({...p,id_number:v}))} ph="13-digit ID" /><UploadBox label="Owner ID Document" uploaded={owner.id_doc} onUpload={()=>setOwner(p=>({...p,id_doc:true}))} icon="🪪" hint="Green ID book or Smart ID" /><div style={{marginTop:14}}><UploadBox label="Owner Selfie" uploaded={owner.selfie} onUpload={()=>setOwner(p=>({...p,selfie:true}))} icon="🤳" hint="Clear face photo" camera /></div><div style={{display:"flex",gap:10,marginTop:20}}><button style={S.btnSecondary} onClick={()=>setStep(0)}>← Back</button><button style={{...S.btnPrimary,flex:1}} onClick={()=>owner.id_doc&&owner.selfie&&setStep(2)}>Next →</button></div></>}
        {step===2&&<><Notice>Upload official documents. PDFs or clear photos accepted.</Notice>{[{key:"cipc",label:"CIPC Registration Certificate",icon:"📄"},{key:"pdp",label:"Operator's Licence / PDP",icon:"🚗"},{key:"roadworthy",label:"Roadworthy Certificate(s)",icon:"🔧"}].map(d=><div key={d.key} style={{marginBottom:14}}><UploadBox label={d.label} uploaded={docs[d.key]} onUpload={()=>setDocs(p=>({...p,[d.key]:true}))} icon={d.icon} hint="PDF or clear photo" /></div>)}<div style={{display:"flex",gap:10,marginTop:8}}><button style={S.btnSecondary} onClick={()=>setStep(1)}>← Back</button><button style={{...S.btnPrimary,flex:1}} onClick={()=>Object.values(docs).every(Boolean)&&setStep(3)}>Next →</button></div></>}
        {step===3&&<><Notice>Each driver needs a valid PDP. Only registered drivers can be assigned to listings.</Notice>{drivers.map(d=><div key={d.id} style={S.addedRow}><span>{d.photo?"🤳":"👤"}</span><span style={{flex:1,fontSize:14}}>{d.name} · PDP: {d.pdp}</span><StatusBadge status="pending" small /></div>)}<div style={S.addSubForm}><p style={S.addSubTitle}>ADD DRIVER</p><FormF label="Name" val={dForm.name} set={v=>setDForm(p=>({...p,name:v}))} ph="Full name" /><FormF label="PDP Number" val={dForm.pdp} set={v=>setDForm(p=>({...p,pdp:v}))} ph="PDP123456" /><FormF label="Phone" val={dForm.phone} set={v=>setDForm(p=>({...p,phone:v}))} ph="+27…" type="tel" /><UploadBox label="Driver Selfie" uploaded={dForm.photo} onUpload={()=>setDForm(p=>({...p,photo:true}))} icon="📷" hint="Clear face photo" camera /><button style={{...S.btnSecondary,marginTop:10}} onClick={()=>{if(dForm.name&&dForm.pdp)setDrivers(p=>[...p,{...dForm,id:"d"+Date.now(),status:"pending"}]);setDForm({name:"",pdp:"",phone:"",photo:false});}}>+ Add Driver</button></div><div style={{display:"flex",gap:10,marginTop:16}}><button style={S.btnSecondary} onClick={()=>setStep(2)}>← Back</button><button style={{...S.btnPrimary,flex:1}} onClick={()=>drivers.length>0&&setStep(4)}>Next ({drivers.length}) →</button></div></>}
        {step===4&&<><Notice>Each vehicle must have a matching roadworthy. Passengers see plate, make and colour.</Notice>{vehicles.map(v=><div key={v.id} style={S.addedRow}><span style={{fontSize:20}}>🚐</span><span style={{flex:1,fontSize:14}}>{v.plate} · {v.make} · {v.seats} seats</span><StatusBadge status="pending" small /></div>)}<div style={S.addSubForm}><p style={S.addSubTitle}>ADD VEHICLE</p><div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:"0 14px"}}><FormF label="Plate" val={vForm.plate} set={v=>setVForm(p=>({...p,plate:v}))} ph="CA 123-456" /><FormF label="Make & Model" val={vForm.make} set={v=>setVForm(p=>({...p,make:v}))} ph="Toyota Quantum" /><FormF label="Seats" val={vForm.seats} set={v=>setVForm(p=>({...p,seats:v}))} ph="16" type="number" /><FormF label="Colour" val={vForm.colour} set={v=>setVForm(p=>({...p,colour:v}))} ph="White" /><FormF label="Roadworthy Until" val={vForm.roadworthy} set={v=>setVForm(p=>({...p,roadworthy:v}))} ph="2027-01" /></div><UploadBox label="Roadworthy Certificate" uploaded={vForm.doc} onUpload={()=>setVForm(p=>({...p,doc:true}))} icon="📋" hint="Valid roadworthy document" /><button style={{...S.btnSecondary,marginTop:10}} onClick={()=>{if(vForm.plate&&vForm.make)setVehicles(p=>[...p,{...vForm,id:"v"+Date.now(),status:"pending"}]);setVForm({plate:"",make:"",seats:"",colour:"",roadworthy:"",doc:false});}}>+ Add Vehicle</button></div><div style={{display:"flex",gap:10,marginTop:16}}><button style={S.btnSecondary} onClick={()=>setStep(3)}>← Back</button><button style={{...S.btnPrimary,flex:1}} onClick={()=>vehicles.length>0&&submit()}>Submit Application →</button></div></>}
        {step===5&&<div style={{textAlign:"center"}}><span style={{fontSize:52}}>📋</span><h3 style={{...S.bigTitle,color:"#fbbf24",marginTop:8,marginBottom:8}}>SUBMITTED</h3><p style={{color:"#666",fontSize:14,lineHeight:1.8,marginBottom:24}}>Documents under review (24–48h).<br/>You'll be contacted on {form.phone} once verified.</p><button style={{...S.btnPrimary,width:"100%"}} onClick={()=>setScreen("operator")}>Go to Operator Portal →</button></div>}
      </div>
    </div>
  );
}

// ─── ADMIN SCREEN ─────────────────────────────────────────────────────────────
function AdminScreen({ ctx, showToast }) {
  const { operators, setOperators, riders, setRiders, events, setEvents, listings } = ctx;
  const [tab, setTab] = useState("overview");

  function verifyOp(id){ setOperators(prev=>prev.map(o=>o.id===id?{...o,status:"verified"}:o)); showToast("Operator verified!"); }
  function rejectOp(id){ setOperators(prev=>prev.map(o=>o.id===id?{...o,status:"rejected"}:o)); showToast("Operator rejected","warn"); }
  function verifyDriver(opId,dId){ setOperators(prev=>prev.map(o=>o.id!==opId?o:{...o,drivers:o.drivers.map(d=>d.id===dId?{...d,status:"verified"}:d)})); showToast("Driver verified!"); }
  function verifyVehicle(opId,vId){ setOperators(prev=>prev.map(o=>o.id!==opId?o:{...o,vehicles:o.vehicles.map(v=>v.id===vId?{...v,status:"verified"}:v)})); showToast("Vehicle verified!"); }
  function verifyRider(id){ setRiders(prev=>prev.map(r=>r.id===id?{...r,status:"verified"}:r)); showToast("Rider verified!"); }

  const pendingOps = operators.filter(o=>o.status==="pending"||o.status==="docs_submitted");
  const pendingRiders = riders.filter(r=>r.status==="id_submitted");

  return (
    <div style={S.page}>
      <SHead title="Admin Dashboard" sub="Verify operators, drivers, vehicles and riders" />
      <div style={{display:"grid",gridTemplateColumns:"repeat(auto-fill,minmax(150px,1fr))",gap:10,marginBottom:24}}>
        {[{label:"Pending Operators",val:pendingOps.length,color:"#fbbf24"},{label:"Verified Operators",val:operators.filter(o=>o.status==="verified").length,color:"#4ade80"},{label:"Pending Riders",val:pendingRiders.length,color:"#fbbf24"},{label:"Verified Riders",val:riders.filter(r=>r.status==="verified").length,color:"#4ade80"},{label:"Total Events",val:events.length,color:"#a78bfa"},{label:"Active Listings",val:listings.length,color:"#c8f04a"}].map(s=>(
          <div key={s.label} style={S.statCard}><div style={{color:"#555",fontSize:11,marginBottom:4}}>{s.label}</div><div style={{color:s.color,fontFamily:"'Bebas Neue',sans-serif",fontSize:30}}>{s.val}</div></div>
        ))}
      </div>

      <div style={S.dashTabs}>
        {[["overview","📊 Overview"],["operators","🚐 Operators"],["riders","🎫 Riders"],["events","🗓 Events"]].map(([t,l])=>(
          <button key={t} onClick={()=>setTab(t)} style={{...S.dashTab,...(tab===t?S.dashTabActive:{})}}>{l}</button>
        ))}
      </div>

      {tab==="overview"&&(
        <div>
          {pendingOps.length>0&&<><SHead title={`${pendingOps.length} Operator${pendingOps.length!==1?"s":""} Awaiting Verification`} />{pendingOps.map(op=>(
            <div key={op.id} style={{...S.adminRow,borderLeft:"3px solid #fbbf24"}}>
              <div style={{display:"flex",gap:10,alignItems:"center"}}><span style={{fontSize:24}}>{op.logo}</span><div><div style={{fontWeight:600}}>{op.name}</div><div style={{color:"#666",fontSize:13}}>{op.owner.email}</div></div></div>
              <div style={{display:"flex",gap:8}}><button style={S.btnDanger} onClick={()=>rejectOp(op.id)}>✗ Reject</button><button style={S.btnSuccess} onClick={()=>verifyOp(op.id)}>✓ Verify</button></div>
            </div>
          ))}</>}
          {pendingRiders.length>0&&<><SHead title={`${pendingRiders.length} Rider${pendingRiders.length!==1?"s":""} Awaiting Verification`} />{pendingRiders.map(r=>(
            <div key={r.id} style={{...S.adminRow,borderLeft:"3px solid #fbbf24"}}>
              <div style={{display:"flex",gap:10,alignItems:"center"}}><div style={{width:36,height:36,background:"#1a1a28",borderRadius:"50%",display:"flex",alignItems:"center",justifyContent:"center",fontSize:20}}>{r.selfie}</div><div><div style={{fontWeight:600}}>{r.name}</div><div style={{color:"#666",fontSize:13}}>ID: {r.id_number}</div></div></div>
              <button style={S.btnSuccess} onClick={()=>verifyRider(r.id)}>✓ Verify</button>
            </div>
          ))}</>}
          {pendingOps.length===0&&pendingRiders.length===0&&<Empty icon="✅" msg="All clear — nothing pending review." />}
        </div>
      )}

      {tab==="operators"&&operators.map(op=>(
        <div key={op.id} style={{...S.adminCard,marginBottom:14}}>
          <div style={{display:"flex",gap:12,alignItems:"flex-start",flexWrap:"wrap"}}>
            <span style={{fontSize:32}}>{op.logo}</span>
            <div style={{flex:1}}>
              <div style={{display:"flex",gap:10,alignItems:"center",flexWrap:"wrap",marginBottom:4}}><span style={{fontWeight:700,fontSize:16}}>{op.name}</span><StatusBadge status={op.status} /></div>
              <div style={{color:"#666",fontSize:13}}>Owner: {op.owner.name} · {op.owner.email}</div>
              <div style={{color:"#666",fontSize:13}}>ID: {op.owner.id_number} · {op.owner.phone}</div>
              <div style={{display:"flex",gap:8,marginTop:6,flexWrap:"wrap"}}>
                {Object.entries(op.docs).map(([k,v])=>(
                  <span key={k} style={{fontSize:11,background:v==="submitted"?"#1a2a00":"#2a1010",color:v==="submitted"?"#4ade80":"#f87171",padding:"2px 8px",borderRadius:4}}>{k}: {v}</span>
                ))}
              </div>
            </div>
            {op.status!=="verified"&&op.status!=="rejected"&&<div style={{display:"flex",gap:8}}><button style={S.btnDanger} onClick={()=>rejectOp(op.id)}>✗</button><button style={S.btnSuccess} onClick={()=>verifyOp(op.id)}>✓ Verify</button></div>}
          </div>
          <div style={{marginTop:12,borderTop:"1px solid #1e1e2a",paddingTop:10}}>
            <p style={S.addSubTitle}>DRIVERS</p>
            {op.drivers.map(d=>(
              <div key={d.id} style={{...S.adminRow,marginBottom:6,padding:"8px 12px"}}>
                <div style={{display:"flex",gap:8,alignItems:"center"}}><span>{d.photo}</span><span style={{fontSize:13}}>{d.name} · PDP: {d.pdp}</span></div>
                <div style={{display:"flex",gap:8,alignItems:"center"}}><StatusBadge status={d.status} small />{d.status!=="verified"&&<button style={{...S.btnSuccess,fontSize:12,padding:"3px 10px"}} onClick={()=>verifyDriver(op.id,d.id)}>Verify</button>}</div>
              </div>
            ))}
            <p style={{...S.addSubTitle,marginTop:10}}>VEHICLES</p>
            {op.vehicles.map(v=>(
              <div key={v.id} style={{...S.adminRow,marginBottom:6,padding:"8px 12px"}}>
                <span style={{fontSize:13}}>🚐 {v.plate} · {v.make} · {v.seats} seats</span>
                <div style={{display:"flex",gap:8,alignItems:"center"}}><StatusBadge status={v.status} small />{v.status!=="verified"&&<button style={{...S.btnSuccess,fontSize:12,padding:"3px 10px"}} onClick={()=>verifyVehicle(op.id,v.id)}>Verify</button>}</div>
              </div>
            ))}
          </div>
        </div>
      ))}

      {tab==="riders"&&riders.map(r=>(
        <div key={r.id} style={{...S.adminRow,marginBottom:10}}>
          <div style={{display:"flex",gap:12,alignItems:"center"}}>
            <div style={{width:40,height:40,background:"#1a1a28",borderRadius:"50%",display:"flex",alignItems:"center",justifyContent:"center",fontSize:20}}>{r.selfie}</div>
            <div><div style={{fontWeight:600}}>{r.name}</div><div style={{color:"#666",fontSize:13}}>{r.email} · {r.phone}</div><div style={{color:"#666",fontSize:12}}>ID: {r.id_number} · {r.bookings} trips · {r.flags} flags</div></div>
          </div>
          <div style={{display:"flex",gap:8,alignItems:"center"}}><StatusBadge status={r.status} />{r.status!=="verified"&&<button style={{...S.btnSuccess,fontSize:12,padding:"6px 14px"}} onClick={()=>verifyRider(r.id)}>✓ Verify</button>}</div>
        </div>
      ))}

      {tab==="events"&&(
        <div>
          {events.map(ev=>(
            <div key={ev.id} style={{...S.adminRow,borderLeft:`3px solid ${ev.color}`}}>
              <div style={{display:"flex",gap:12,alignItems:"center"}}><span style={{fontSize:28}}>{ev.banner}</span><div><div style={{fontWeight:600}}>{ev.name}</div><div style={{color:"#666",fontSize:13}}>{ev.venue} · {ev.dates.join(", ")}</div></div></div>
              <div style={{color:"#555",fontSize:13}}>{listings.filter(l=>l.eventId===ev.id).length} listings</div>
            </div>
          ))}
        </div>
      )}
    </div>
  );
}

// ─── SMALL COMPONENTS ─────────────────────────────────────────────────────────
function SHead({ title, sub, action }) {
  return (
    <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-end",marginBottom:16}}>
      <div><h2 style={S.secTitle}>{title}</h2>{sub&&<p style={S.secSub}>{sub}</p>}</div>
      {action&&<button style={{background:"none",border:"none",color:"#c8f04a",fontSize:13,cursor:"pointer"}} onClick={action.onClick}>{action.label}</button>}
    </div>
  );
}
function Pill({ active, onClick, children }) {
  return <button onClick={onClick} style={{...S.pill,...(active?S.pillActive:{})}}>{children}</button>;
}
function FilterRow({ label, children }) {
  return <div style={{display:"flex",gap:8,alignItems:"center",flexWrap:"wrap"}}><span style={{fontSize:11,color:"#444",textTransform:"uppercase",letterSpacing:1.5,minWidth:60}}>{label}</span><div style={{display:"flex",gap:6,flexWrap:"wrap"}}>{children}</div></div>;
}
function StepBar({ steps, current }) {
  return (
    <div style={{display:"flex",alignItems:"center",justifyContent:"center",flexWrap:"wrap",padding:"14px 0 22px"}}>
      {steps.map((s,i)=>(
        <div key={s} style={{display:"flex",alignItems:"center",gap:6}}>
          <div style={{width:26,height:26,borderRadius:"50%",border:"2px solid",borderColor:i<current?"#4ade80":i===current?"#c8f04a":"#2a2a3a",background:i<current?"#4ade80":i===current?"#c8f04a":"transparent",display:"flex",alignItems:"center",justifyContent:"center",fontSize:11,fontWeight:700,color:i<=current?"#000":"#555",flexShrink:0}}>{i<current?"✓":i+1}</div>
          <span style={{fontSize:12,color:i===current?"#c8f04a":"#555",marginRight:4}}>{s}</span>
          {i<steps.length-1&&<div style={{width:18,height:2,background:i<current?"#4ade80":"#1e1e2a",marginRight:4}} />}
        </div>
      ))}
    </div>
  );
}
function StatusBadge({ status, small }) {
  const c=STATUS_COLORS[status]||"#666";
  return <span style={{fontSize:small?11:12,background:c+"22",color:c,border:`1px solid ${c}44`,padding:small?"1px 7px":"3px 10px",borderRadius:20,whiteSpace:"nowrap"}}>{STATUS_LABELS[status]||status}</span>;
}
function Notice({ children }) { return <div style={S.notice}>{children}</div>; }
function FlashMsg({ children }) { return <div style={{background:"#0d1f0d",border:"1px solid #4ade8033",borderRadius:8,padding:"10px 14px",color:"#4ade80",fontSize:13,marginBottom:14}}>{children}</div>; }
function Empty({ icon, msg }) { return <div style={{textAlign:"center",padding:"40px 20px",color:"#444",display:"flex",flexDirection:"column",gap:10,alignItems:"center"}}><span style={{fontSize:36}}>{icon}</span><p>{msg}</p></div>; }
function ErrTxt({ children }) { return <span style={{color:"#f87171",fontSize:12,marginTop:3,display:"block"}}>{children}</span>; }
function FormF({ label, val, set, ph, type="text", err }) {
  return <div style={{marginBottom:14}}><label style={S.formLbl}>{label}</label><input style={{...S.inp,...(err?{borderColor:"#f87171"}:{})}} value={val} onChange={e=>set(e.target.value)} placeholder={ph} type={type} />{err&&<ErrTxt>{err}</ErrTxt>}</div>;
}
function SelF({ label, val, set, children }) {
  return <div style={{marginBottom:14}}><label style={S.formLbl}>{label}</label><select style={S.inp} value={val} onChange={e=>set(e.target.value)}>{children}</select></div>;
}
function UploadBox({ label, uploaded, onUpload, icon, hint, camera }) {
  return <div onClick={onUpload} style={{...S.uploadBox,...(uploaded?{borderColor:"#4ade80",background:"#0d1f0d"}:{})}}><span style={{fontSize:26}}>{uploaded?"✅":icon}</span><div><div style={{fontSize:14,fontWeight:500,color:uploaded?"#4ade80":"#aaa"}}>{uploaded?label+" uploaded":label}</div>{!uploaded&&<div style={{fontSize:12,color:"#555",marginTop:2}}>{camera?"📷 ":"📎 "}{hint} · Click to upload</div>}</div></div>;
}
function ReviewCard({ review }) {
  return <div style={{background:"#0d0d12",border:"1px solid #14141e",borderRadius:10,padding:"14px 16px"}}><div style={{display:"flex",justifyContent:"space-between",marginBottom:6}}><span style={{fontWeight:600,fontSize:13}}>{review.riderName}</span><span style={{color:"#555",fontSize:12}}>{review.date}</span></div><div style={{color:"#f0a030",marginBottom:6,fontSize:14}}>{stars(review.rating)}</div><p style={{color:"#aaa",fontSize:13,lineHeight:1.6}}>{review.comment}</p></div>;
}

// ─── STYLES ───────────────────────────────────────────────────────────────────
const GLOBAL_CSS = `
  @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@400;500;600;700;800&display=swap');
  *{box-sizing:border-box;margin:0;padding:0;}
  body{background:#060609;overscroll-behavior:none;}
  input,select,textarea,button{font-family:'Syne',sans-serif;}
  ::-webkit-scrollbar{width:4px;} ::-webkit-scrollbar-thumb{background:#222;border-radius:2px;}
  .ev-card:hover{transform:translateY(-3px);border-color:#ffffff1a!important;}
  .lst-card:hover{border-color:#ffffff22!important;}
  .hovcard:hover{transform:translateY(-2px);border-color:#ffffff1a!important;}
  .book-btn:hover{filter:brightness(1.12);}
  .card-hover:hover{border-color:#c8f04a55!important;}
  .set-row:hover{background:#0f0f16!important;}
  input[type=range]{accent-color:#c8f04a;}
  textarea{resize:vertical;}
`;

const S = {
  root:{ minHeight:"100vh", background:"#060609", color:"#ddd", fontFamily:"'Syne',sans-serif", paddingBottom:70 },
  wrap:{ maxWidth:920, margin:"0 auto" },

  // NAV
  nav:{ height:56, background:"#08080c", borderBottom:"1px solid #111118", display:"flex", alignItems:"center", justifyContent:"space-between", padding:"0 16px", position:"sticky", top:0, zIndex:200 },
  navBrand:{ display:"flex", alignItems:"center", gap:10, background:"none", border:"none", cursor:"pointer", padding:0 },
  logoBox:{ width:30, height:30, background:"#c8f04a", borderRadius:6, color:"#000", fontFamily:"'Bebas Neue',sans-serif", fontSize:20, display:"flex", alignItems:"center", justifyContent:"center" },
  logoWord:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:22, letterSpacing:3, color:"#ddd" },
  navLinks:{ display:"flex", gap:2 },
  navBtn:{ padding:"7px 12px", background:"none", border:"none", color:"#555", cursor:"pointer", borderRadius:6, display:"flex", flexDirection:"column", alignItems:"center", gap:1, transition:"all 0.15s", fontSize:12 },
  navBtnIcon:{ fontSize:16 },
  navBtnLabel:{ fontSize:10, letterSpacing:0.5 },
  navBtnActive:{ background:"#14141e", color:"#ddd" },

  // BOTTOM NAV
  bottomNav:{ position:"fixed", bottom:0, left:0, right:0, background:"#08080c", borderTop:"1px solid #111118", display:"flex", zIndex:200, height:60 },
  bnBtn:{ flex:1, background:"none", border:"none", color:"#555", cursor:"pointer", display:"flex", flexDirection:"column", alignItems:"center", justifyContent:"center", gap:2, transition:"all 0.15s" },
  bnBtnActive:{ color:"#c8f04a" },

  // TOAST
  toast:{ position:"fixed", top:68, right:16, border:"1px solid", borderRadius:8, padding:"10px 16px", fontSize:13, fontWeight:500, zIndex:999, boxShadow:"0 4px 20px #00000066" },

  // PAGE
  page:{ padding:"24px 16px 40px", maxWidth:920, margin:"0 auto" },
  backBtn:{ background:"none", border:"none", color:"#555", cursor:"pointer", fontSize:14, marginBottom:20, padding:0, display:"block" },
  section:{ marginBottom:40 },

  // HERO
  hero:{ position:"relative", textAlign:"center", padding:"52px 16px 40px", marginBottom:32, overflow:"hidden" },
  heroBg:{ position:"absolute", inset:0, background:"radial-gradient(ellipse at 50% 0%, #c8f04a0a 0%, transparent 70%)", pointerEvents:"none" },
  heroEye:{ fontSize:11, letterSpacing:4, color:"#444", textTransform:"uppercase", marginBottom:14 },
  heroH1:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:"clamp(52px,12vw,108px)", letterSpacing:4, color:"#e8e8e8", lineHeight:1, marginBottom:14 },
  heroSub:{ color:"#555", fontSize:14, marginBottom:28 },
  heroSearch:{ maxWidth:460, margin:"0 auto 28px", position:"relative" },
  heroSearchIcon:{ position:"absolute", left:14, top:"50%", transform:"translateY(-50%)", fontSize:16 },
  heroSearchInp:{ width:"100%", padding:"13px 14px 13px 44px", background:"#0f0f14", border:"1.5px solid #1e1e2a", borderRadius:12, color:"#ddd", fontSize:15, outline:"none" },
  heroStats:{ display:"flex", gap:0, justifyContent:"center", background:"#0c0c12", border:"1px solid #141420", borderRadius:12, padding:"14px 0", maxWidth:400, margin:"0 auto" },
  heroStat:{ flex:1, display:"flex", flexDirection:"column", alignItems:"center", gap:4 },
  heroStatNum:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:28, color:"#c8f04a", lineHeight:1 },
  heroStatLbl:{ fontSize:11, color:"#555", textAlign:"center" },
  heroStatDiv:{ width:1, background:"#1e1e2a" },

  // TRUST STRIP
  trustStrip:{ display:"flex", gap:0, background:"#0c0c12", border:"1px solid #141420", borderRadius:12, marginBottom:36, overflow:"hidden", flexWrap:"wrap" },
  trustItem:{ flex:"1 1 180px", display:"flex", gap:12, alignItems:"center", padding:"14px 16px", borderRight:"1px solid #141420" },
  trustIcon:{ fontSize:22, flexShrink:0 },
  trustTitle:{ fontSize:13, fontWeight:600, color:"#ddd" },
  trustSub:{ fontSize:11, color:"#555", marginTop:2 },

  // HOW IT WORKS
  howGrid:{ display:"grid", gridTemplateColumns:"repeat(auto-fill,minmax(180px,1fr))", gap:12 },
  howCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:12, padding:"20px 16px" },
  howNum:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:42, color:"#c8f04a22", lineHeight:1, marginBottom:4 },
  howTitle:{ fontWeight:700, fontSize:14, marginBottom:6 },
  howDesc:{ fontSize:12, color:"#555", lineHeight:1.6 },

  // SEARCH
  searchRow:{ marginBottom:16 },
  searchBox:{ position:"relative", maxWidth:500 },
  searchInp:{ width:"100%", padding:"11px 36px 11px 36px", background:"#0f0f14", border:"1.5px solid #1e1e2a", borderRadius:10, color:"#ddd", fontSize:14, outline:"none" },
  searchClear:{ position:"absolute", right:10, top:"50%", transform:"translateY(-50%)", background:"none", border:"none", color:"#555", cursor:"pointer", fontSize:14 },

  // FILTER BLOCK
  filterBlock:{ background:"#0c0c10", border:"1px solid #14141e", borderRadius:12, padding:"14px 16px", marginBottom:20, display:"flex", flexDirection:"column", gap:12 },
  pill:{ padding:"5px 13px", background:"#0f0f14", border:"1px solid #1a1a24", borderRadius:20, color:"#555", cursor:"pointer", fontSize:12, transition:"all 0.15s", fontFamily:"'Syne',sans-serif" },
  pillActive:{ background:"#1a1a28", borderColor:"#ffffff33", color:"#ddd" },

  // PRICE RANGE
  priceRangeBar:{ display:"flex", alignItems:"center", justifyContent:"space-between", background:"#0c0c10", border:"1px solid #14141e", borderRadius:10, padding:"10px 16px", marginBottom:14, gap:16 },
  rangeSlider:{ flex:1, maxWidth:200 },

  // EVENT GRID
  eventGrid:{ display:"grid", gridTemplateColumns:"repeat(auto-fill,minmax(270px,1fr))", gap:14 },
  evCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:14, padding:"20px 18px", cursor:"pointer", transition:"all 0.22s" },
  evCardTop:{ display:"flex", justifyContent:"space-between", alignItems:"flex-start", marginBottom:12 },
  typePill:{ fontSize:11, padding:"3px 9px", borderRadius:20, fontWeight:500 },
  saveBtn:{ background:"none", border:"none", cursor:"pointer", fontSize:20, lineHeight:1, padding:0 },
  evName:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:22, letterSpacing:1, color:"#e8e8e8", marginBottom:5, lineHeight:1.1 },
  evVenue:{ fontSize:12, color:"#555", marginBottom:3 },
  evDates:{ fontSize:12, color:"#555", marginBottom:6 },
  evLineup:{ fontSize:12, color:"#777", fontStyle:"italic", marginBottom:8 },
  evFoot:{ display:"flex", justifyContent:"space-between", alignItems:"center", paddingTop:10, borderTop:"1px solid #141420", marginTop:8 },

  // EVENT HERO
  evHero:{ display:"flex", gap:18, marginBottom:28, paddingBottom:24, flexWrap:"wrap" },
  evHeroTitle:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:"clamp(28px,5vw,52px)", letterSpacing:2, lineHeight:1, marginBottom:8 },
  evHeroMeta:{ color:"#666", fontSize:13, marginBottom:3 },

  // LISTING CARD
  lstCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:14, overflow:"hidden", transition:"all 0.2s" },
  lstAccent:{ height:3 },
  lstBody:{ padding:"18px 20px" },
  lstTop:{ display:"flex", justifyContent:"space-between", alignItems:"flex-start", marginBottom:12 },
  lstOpRow:{ display:"flex", gap:10, alignItems:"center" },
  lstPriceCol:{ display:"flex", flexDirection:"column", alignItems:"flex-end" },
  lstPrice:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:34, lineHeight:1 },
  lstPP:{ fontSize:11, color:"#555" },
  lstRoute:{ display:"flex", gap:10, alignItems:"center", flexWrap:"wrap", marginBottom:8 },
  lstLocChip:{ background:"#141420", border:"1px solid #1e1e2a", borderRadius:6, padding:"3px 10px", fontSize:13 },
  lstMeta:{ display:"flex", gap:14, flexWrap:"wrap", color:"#555", fontSize:13, marginBottom:10 },
  amenityRow:{ display:"flex", gap:6, flexWrap:"wrap", marginBottom:10 },
  amenityChip:{ background:"#141420", border:"1px solid #1e1e2a", borderRadius:20, padding:"2px 9px", fontSize:11, color:"#888" },
  driverVehicleStrip:{ display:"flex", gap:16, flexWrap:"wrap", borderTop:"1px solid #14141e", paddingTop:10, marginBottom:12 },
  dvItem:{ display:"flex", gap:8, alignItems:"center" },
  dvAvatar:{ width:32, height:32, background:"#1a1a24", borderRadius:"50%", display:"flex", alignItems:"center", justifyContent:"center", fontSize:18 },
  lstBtns:{ display:"flex", gap:10, justifyContent:"flex-end" },
  waBtn:{ padding:"8px 14px", background:"#1dab5511", border:"1px solid #1dab5544", borderRadius:8, color:"#1dab55", fontSize:13, fontWeight:600, cursor:"pointer", textDecoration:"none" },
  bookBtn:{ padding:"9px 20px", border:"none", borderRadius:8, color:"#000", fontSize:14, fontWeight:700, cursor:"pointer", transition:"all 0.15s" },

  // BOOK FLOW
  bookCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:14, padding:"24px 22px", maxWidth:560, margin:"0 auto" },
  bookEventBanner:{ display:"flex", gap:14, alignItems:"center", background:"#0c0c10", borderRadius:10, padding:"12px 16px", marginBottom:16 },
  trustCard:{ background:"#0a0a0e", border:"1px solid #1a1a24", borderRadius:10, padding:"14px 16px", marginBottom:12 },
  trustMicroTitle:{ fontSize:10, color:"#444", letterSpacing:2, textTransform:"uppercase", marginBottom:8 },
  driverRow:{ display:"flex", gap:12, alignItems:"center" },
  driverAvatar:{ width:40, height:40, background:"#1a1a24", borderRadius:"50%", display:"flex", alignItems:"center", justifyContent:"center", fontSize:22, flexShrink:0 },
  totalBar:{ display:"flex", justifyContent:"space-between", alignItems:"center", background:"#0c0c10", border:"1px solid", borderRadius:10, padding:"12px 16px", margin:"14px 0 8px" },
  totalAmt:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:34 },
  cardSelectRow:{ display:"flex", gap:12, alignItems:"center", background:"#0d0d12", border:"1px solid #1a1a24", borderRadius:8, padding:"10px 14px", marginBottom:6, cursor:"pointer" },

  // CONFIRM
  confirmWrap:{ maxWidth:520, margin:"0 auto", background:"#0d0d12", border:"1px solid #14141e", borderRadius:16, padding:"32px 24px" },
  confirmBox:{ background:"#0a0a0e", border:"1px solid #1e1e2a", borderRadius:10, padding:"14px 16px", marginBottom:16 },
  cRow:{ display:"flex", justifyContent:"space-between", padding:"7px 0", borderBottom:"1px solid #14141e" },
  cLbl:{ fontSize:12, color:"#555", textTransform:"uppercase", letterSpacing:1 },
  cVal:{ fontSize:14, textAlign:"right" },
  bigTitle:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:38, letterSpacing:3, textAlign:"center" },

  // ACCOUNT
  acctHeader:{ display:"flex", gap:16, alignItems:"center", marginBottom:24, padding:"18px 20px", background:"#0d0d12", border:"1px solid #14141e", borderRadius:14 },
  acctAvatarWrap:{ position:"relative", flexShrink:0 },
  acctAvatar:{ width:72, height:72, background:"#1a1a24", borderRadius:"50%", display:"flex", alignItems:"center", justifyContent:"center" },
  acctAvatarBadge:{ position:"absolute", bottom:-4, right:-4 },
  acctName:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:26, letterSpacing:2, marginBottom:4 },
  acctStat:{ fontSize:13, color:"#555", background:"#12121a", padding:"3px 10px", borderRadius:20 },
  settCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:14, padding:"22px 20px" },
  selfieRow:{ display:"flex", gap:16, alignItems:"flex-start", marginBottom:18 },
  selfieCircle:{ width:76, height:76, background:"#1a1a24", borderRadius:"50%", display:"flex", alignItems:"center", justifyContent:"center", flexShrink:0, position:"relative", border:"2px solid #2a2a3a" },
  selfieCheck:{ position:"absolute", bottom:0, right:0, background:"#4ade80", color:"#000", width:20, height:20, borderRadius:"50%", display:"flex", alignItems:"center", justifyContent:"center", fontSize:11, fontWeight:700 },
  idLocked:{ fontFamily:"monospace", color:"#aaa", background:"#12121a", border:"1.5px solid #1e1e2a", borderRadius:8, padding:"10px 13px", marginTop:6, letterSpacing:2, display:"flex", justifyContent:"space-between", alignItems:"center", flexWrap:"wrap", gap:8 },
  dangerZone:{ background:"#100a0a", border:"1px solid #2a1414", borderRadius:10, padding:"14px 16px" },

  // VERIFICATION
  verBanner:{ display:"flex", gap:14, alignItems:"center", borderRadius:12, padding:"16px 18px", border:"1px solid", marginBottom:8 },
  verDot:{ width:28, height:28, borderRadius:"50%", border:"2px solid", display:"flex", alignItems:"center", justifyContent:"center", fontSize:12, fontWeight:700, flexShrink:0, marginTop:2 },

  // CARDS
  cardRow:{ background:"#0a0a0e", border:"1px solid #1a1a24", borderRadius:12, padding:"16px 18px", marginBottom:10, display:"flex", gap:16, alignItems:"center", flexWrap:"wrap", transition:"all 0.2s" },
  cardVisual:{ flex:1, minWidth:200 },
  cardChip:{ width:28, height:20, background:"#fbbf24", borderRadius:4, marginBottom:12 },
  primaryBadge:{ fontSize:12, color:"#c8f04a", background:"#1a2200", border:"1px solid #c8f04a33", padding:"3px 10px", borderRadius:20 },
  setDefBtn:{ fontSize:12, color:"#888", background:"none", border:"1px solid #2a2a3a", borderRadius:20, padding:"3px 10px", cursor:"pointer" },
  removeCardBtn:{ fontSize:12, color:"#f87171", background:"none", border:"1px solid #2a1414", borderRadius:20, padding:"3px 10px", cursor:"pointer" },
  addCardWrap:{ background:"#0a0a0e", border:"1px solid #1a1a24", borderRadius:10, padding:"16px 18px", marginTop:8 },

  // NOTIFICATIONS
  notifRow:{ display:"flex", alignItems:"center", justifyContent:"space-between", padding:"14px 0", borderBottom:"1px solid #14141e", cursor:"pointer" },
  toggle:{ width:44, height:24, borderRadius:12, transition:"background 0.2s", position:"relative", flexShrink:0 },
  toggleThumb:{ position:"absolute", top:2, width:20, height:20, background:"#fff", borderRadius:"50%", transition:"transform 0.2s" },

  // REVIEW
  reviewWrap:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:12, padding:"16px 18px" },

  // OPERATOR
  opGrid:{ display:"grid", gridTemplateColumns:"repeat(auto-fill,minmax(200px,1fr))", gap:12 },
  opCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:12, padding:"18px 16px", cursor:"pointer", transition:"all 0.2s" },

  // ADMIN
  adminRow:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:10, padding:"12px 16px", marginBottom:8, display:"flex", justifyContent:"space-between", alignItems:"center", flexWrap:"wrap", gap:10 },
  adminCard:{ background:"#0d0d12", border:"1px solid #1a1a24", borderRadius:12, padding:"16px 18px" },
  statCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:10, padding:"14px 16px" },
  statusChip:{ fontSize:12, padding:"3px 10px", borderRadius:20, display:"inline-block", marginTop:4 },
  bookingCard:{ background:"#0d0d12", border:"1px solid #14141e", borderRadius:12, padding:"14px 16px", marginBottom:10 },

  // SHARED
  dashTabs:{ display:"flex", borderBottom:"1px solid #14141e", marginBottom:22, overflowX:"auto" },
  dashTab:{ padding:"10px 16px", background:"none", border:"none", borderBottom:"2px solid transparent", color:"#555", cursor:"pointer", fontSize:13, fontWeight:500, fontFamily:"'Syne',sans-serif", transition:"all 0.15s", whiteSpace:"nowrap" },
  dashTabActive:{ color:"#ddd", borderBottom:"2px solid #c8f04a" },
  secTitle:{ fontFamily:"'Bebas Neue',sans-serif", fontSize:24, letterSpacing:2, color:"#e0e0e0" },
  secSub:{ color:"#555", fontSize:13, marginTop:3 },
  notice:{ background:"#12121a", border:"1px solid #1e1e2a", borderRadius:8, padding:"10px 14px", fontSize:13, color:"#666", lineHeight:1.6, marginBottom:12 },
  formPanel:{ background:"#0d0d12", border:"1px solid #1a1a24", borderRadius:14, padding:"22px 20px", maxWidth:540, margin:"0 auto" },
  formLbl:{ display:"block", fontSize:11, textTransform:"uppercase", letterSpacing:1.2, color:"#555", marginBottom:5 },
  inp:{ width:"100%", padding:"10px 13px", background:"#12121a", border:"1.5px solid #1e1e2a", borderRadius:8, color:"#ddd", fontSize:14, outline:"none" },
  addSubForm:{ background:"#0a0a0e", border:"1px solid #1a1a24", borderRadius:10, padding:"16px 18px", marginTop:14 },
  addSubTitle:{ fontSize:10, letterSpacing:2, color:"#444", textTransform:"uppercase", marginBottom:12 },
  addedRow:{ display:"flex", gap:10, alignItems:"center", background:"#0d0d12", border:"1px solid #1a1a24", borderRadius:8, padding:"10px 14px", marginBottom:8 },
  uploadBox:{ display:"flex", gap:14, alignItems:"center", background:"#0d0d12", border:"2px dashed #1e1e2a", borderRadius:10, padding:"14px 16px", cursor:"pointer", transition:"all 0.15s", marginBottom:4 },
  cntBtn:{ width:32, height:32, borderRadius:"50%", background:"#1a1a24", border:"1px solid #22222e", color:"#ddd", fontSize:18, cursor:"pointer", display:"flex", alignItems:"center", justifyContent:"center" },
  btnPrimary:{ padding:"11px 24px", background:"#c8f04a", border:"none", borderRadius:8, color:"#000", fontWeight:700, fontSize:14, cursor:"pointer", fontFamily:"'Syne',sans-serif" },
  btnSecondary:{ padding:"11px 20px", background:"none", border:"1.5px solid #1e1e2a", borderRadius:8, color:"#666", fontWeight:600, fontSize:13, cursor:"pointer", fontFamily:"'Syne',sans-serif" },
  btnSuccess:{ padding:"8px 16px", background:"#14280a", border:"1px solid #4ade8044", color:"#4ade80", borderRadius:7, cursor:"pointer", fontSize:13, fontFamily:"'Syne',sans-serif" },
  btnDanger:{ padding:"8px 14px", background:"#1a0a0a", border:"1px solid #f8717144", color:"#f87171", borderRadius:7, cursor:"pointer", fontSize:13, fontFamily:"'Syne',sans-serif" },
  delBtn:{ padding:"5px 10px", background:"#1a0808", border:"1px solid #3a1414", borderRadius:6, color:"#f87171", cursor:"pointer", fontSize:13 },
  footer:{ borderTop:"1px solid #0f0f14", padding:"16px", textAlign:"center", fontSize:11, color:"#333" },
};
