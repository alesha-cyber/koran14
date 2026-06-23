<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KORAN PALASTA – SKOR &amp; PENGHARGAAN SMPN 14 Tangerang</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --merah-tua:   #8B0000;
    --merah:       #B91C1C;
    --merah-mid:   #CC2200;
    --kuning:      #D4A017;
    --kuning-muda: #F4C842;
    --krem:        #FDF8F0;
    --abu:         #6B7280;
    --gelap:       #1A1A1A;
    --putih:       #FFFFFF;
    --hijau:       #166534;
    --oranye:      #D97706;
    --biru:        #1D4ED8;
  }
  body { font-family: "Segoe UI", system-ui, sans-serif; background: var(--krem); color: var(--gelap); min-height: 100vh; }

  /* HEADER */
  header {
    background: linear-gradient(135deg, #7B0000 0%, #B91C1C 60%, #CC2200 100%);
    color: var(--putih);
    position: sticky; top: 0; z-index: 100;
    box-shadow: 0 3px 16px rgba(0,0,0,.4);
  }
  .header-inner {
    max-width: 1120px; margin: auto;
    padding: 14px 24px;
    display: flex; align-items: center; gap: 16px;
  }
  .logo-img { width: 58px; height: 58px; object-fit: contain; flex-shrink: 0; filter: drop-shadow(0 2px 4px rgba(0,0,0,.4)); }
  .divider-v { width: 2px; height: 48px; background: rgba(255,255,255,.3); border-radius: 2px; flex-shrink: 0; }
  .header-text h1 { font-size: 17px; font-weight: 800; letter-spacing: .3px; }
  .header-text p  { font-size: 11px; opacity: .8; margin-top: 3px; }
  .header-badge {
    margin-left: auto;
    background: rgba(255,255,255,.15);
    border: 1px solid rgba(255,255,255,.3);
    border-radius: 20px;
    padding: 6px 14px;
    font-size: 11px;
    font-weight: 600;
    white-space: nowrap;
  }

  /* TABS */
  .tabs { background: #6B0000; border-top: 1px solid rgba(255,255,255,.1); }
  .tabs-inner { max-width: 1120px; margin: auto; display: flex; overflow-x: auto; }
  .tab-btn {
    padding: 11px 20px; background: none; border: none;
    color: rgba(255,255,255,.55); font-size: 12.5px; font-weight: 600;
    cursor: pointer; border-bottom: 3px solid transparent;
    transition: all .18s; white-space: nowrap; letter-spacing: .3px;
  }
  .tab-btn:hover { color: var(--putih); background: rgba(255,255,255,.07); }
  .tab-btn.active { color: var(--kuning-muda); border-bottom-color: var(--kuning-muda); }

  /* MAIN */
  main { max-width: 1120px; margin: 26px auto; padding: 0 18px; }
  .section { display: none; }
  .section.active { display: block; }

  /* CARD */
  .card { background: var(--putih); border-radius: 12px; box-shadow: 0 1px 6px rgba(0,0,0,.08); padding: 22px 24px; margin-bottom: 18px; }
  .card-title {
    font-size: 14.5px; font-weight: 700; color: var(--merah-tua);
    margin-bottom: 16px; display: flex; align-items: center; gap: 8px;
  }
  .card-title::before { content:''; display:inline-block; width:4px; height:17px; background:var(--kuning); border-radius:2px; }

  /* FORM */
  .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 13px; }
  .form-grid .full { grid-column: 1/-1; }
  label { font-size: 11.5px; font-weight: 600; color: var(--abu); display: block; margin-bottom: 4px; text-transform: uppercase; letter-spacing: .4px; }
  input, select, textarea {
    width: 100%; padding: 10px 12px;
    border: 1.5px solid #E5E7EB; border-radius: 8px;
    font-size: 13.5px; background: #FAFAFA; transition: border .2s; color: var(--gelap);
  }
  input:focus, select:focus, textarea:focus { outline: none; border-color: var(--merah); background: var(--putih); }

  /* BUTTONS */
  .btn { padding: 10px 20px; border: none; border-radius: 8px; font-size: 13.5px; font-weight: 600; cursor: pointer; transition: all .16s; }
  .btn-primary { background: var(--merah); color: var(--putih); }
  .btn-primary:hover { background: var(--merah-tua); transform: translateY(-1px); }
  .btn-success { background: #D1FAE5; color: #065F46; }
  .btn-success:hover { background: #A7F3D0; }
  .btn-warning { background: #FEF3C7; color: #92400E; }
  .btn-warning:hover { background: #FDE68A; }
  .btn-danger { background: #FEE2E2; color: var(--merah); }
  .btn-danger:hover { background: #FECACA; }
  .btn-sm { padding: 6px 12px; font-size: 12px; }

  /* STATUS BAR */
  .status-bar { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px,1fr)); gap: 12px; margin-bottom: 20px; }
  .status-item { background: var(--putih); border-radius: 10px; padding: 16px; text-align: center; box-shadow: 0 1px 4px rgba(0,0,0,.07); border-top: 4px solid #2D6A4F; }
  .status-item.kuning { border-top-color: var(--kuning); }
  .status-item.merah  { border-top-color: var(--merah); }
  .status-item.hitam  { border-top-color: #1F2937; }
  .status-num { font-size: 28px; font-weight: 900; color: #1F2937; }
  .status-num.merah { color: var(--merah); }
  .status-num.kuning { color: var(--oranye); }
  .status-label { font-size: 10.5px; color: var(--abu); margin-top: 4px; font-weight: 600; text-transform: uppercase; letter-spacing: .5px; }

  /* SANKSI BADGE */
  .sanksi-badge { display: inline-flex; align-items: center; gap: 5px; padding: 5px 13px; border-radius: 20px; font-size: 12px; font-weight: 700; }
  .sanksi-aman   { background: #D1FAE5; color: #065F46; }
  .sanksi-ringan { background: #FEF3C7; color: #92400E; }
  .sanksi-sedang { background: #FED7AA; color: #7C2D12; }
  .sanksi-berat  { background: #FEE2E2; color: var(--merah); }
  .sanksi-kritis { background: #7F1D1D; color: var(--putih); }

  /* TABLE */
  .tbl-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; font-size: 13px; }
  th { background: var(--merah-tua); color: var(--putih); padding: 10px 13px; text-align: left; font-size: 11.5px; letter-spacing: .4px; }
  td { padding: 9px 13px; border-bottom: 1px solid #F0F0F0; }
  tr:hover td { background: #FFF8F8; }
  .td-poin { font-weight: 700; color: var(--merah); text-align: center; }
  .td-center { text-align: center; }

  /* BADGE */
  .badge { display: inline-block; padding: 3px 9px; border-radius: 12px; font-size: 10.5px; font-weight: 700; }
  .badge-ringan { background: #FEF3C7; color: #92400E; }
  .badge-sedang { background: #FED7AA; color: #7C2D12; }
  .badge-berat  { background: #FEE2E2; color: var(--merah); }

  /* PROGRESS */
  .progress-wrap { background: #E5E7EB; border-radius: 99px; height: 9px; overflow: hidden; }
  .progress-bar  { height: 100%; border-radius: 99px; transition: width .4s; }

  /* SEARCH ROW */
  .search-row { display: flex; gap: 10px; margin-bottom: 14px; flex-wrap: wrap; }
  .search-row input  { flex: 1; min-width: 160px; }
  .search-row select { width: 150px; }

  /* SISWA CARD */
  .siswa-card {
    background: var(--putih); border-radius: 11px; padding: 16px 18px;
    display: flex; align-items: center; gap: 14px;
    box-shadow: 0 1px 4px rgba(0,0,0,.07);
    margin-bottom: 10px; cursor: pointer; transition: all .14s;
    border: 2px solid transparent;
  }
  .siswa-card:hover { border-color: var(--merah); transform: translateY(-1px); }
  .siswa-avatar {
    width: 46px; height: 46px; border-radius: 50%;
    background: linear-gradient(135deg, #B91C1C, #7B0000);
    color: var(--putih); display: flex; align-items: center; justify-content: center;
    font-size: 17px; font-weight: 800; flex-shrink: 0;
  }
  .siswa-info { flex: 1; min-width: 0; }
  .siswa-nama { font-weight: 700; font-size: 14.5px; }
  .siswa-meta { font-size: 11.5px; color: var(--abu); margin-top: 2px; }
  .siswa-poin-total { font-size: 22px; font-weight: 900; flex-shrink: 0; }

  /* RIWAYAT */
  .riwayat-item { display: flex; align-items: flex-start; gap: 11px; padding: 11px 0; border-bottom: 1px solid #F3F4F6; }
  .riwayat-icon { width: 34px; height: 34px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 15px; flex-shrink: 0; }
  .riwayat-info { flex: 1; min-width: 0; }
  .riwayat-nama   { font-weight: 700; font-size: 13.5px; }
  .riwayat-detail { font-size: 11.5px; color: var(--abu); margin-top: 2px; }
  .riwayat-poin   { font-weight: 800; font-size: 15px; color: var(--merah); flex-shrink: 0; }

  /* MODAL */
  .modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,.55); z-index: 999; align-items: center; justify-content: center; padding: 20px; }
  .modal-overlay.show { display: flex; }
  .modal { background: var(--putih); border-radius: 14px; padding: 26px; max-width: 500px; width: 100%; box-shadow: 0 20px 60px rgba(0,0,0,.3); animation: slideUp .22s ease; max-height: 90vh; overflow-y: auto; }
  @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
  .modal h2 { font-size: 16px; margin-bottom: 14px; color: var(--merah-tua); }

  /* SANKSI PANEL */
  .sanksi-panel { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .sanksi-tier { border-radius: 10px; padding: 13px; border-left: 4px solid; }
  .sanksi-tier.ringan { background: #FFFBEB; border-color: #F59E0B; }
  .sanksi-tier.sedang { background: #FFF7ED; border-color: #F97316; }
  .sanksi-tier.berat  { background: #FEF2F2; border-color: var(--merah); }
  .sanksi-tier.kritis { background: #7F1D1D; border-color: #450A0A; color: var(--putih); }
  .sanksi-tier h4  { font-size: 12.5px; font-weight: 700; margin-bottom: 5px; }
  .sanksi-tier h4.sub { margin-top: 10px; }
  .sanksi-tier ul  { padding-left: 15px; font-size: 11.5px; line-height: 1.7; }

  /* IMPORT / EXPORT AREA */
  .upload-area {
    border: 2.5px dashed #D1D5DB; border-radius: 12px;
    padding: 28px; text-align: center; cursor: pointer;
    transition: all .2s; background: #FAFAFA;
  }
  .upload-area:hover { border-color: var(--merah); background: #FFF8F8; }
  .upload-area .icon { font-size: 36px; margin-bottom: 8px; }
  .upload-area p { font-size: 13px; color: var(--abu); }
  .upload-area strong { color: var(--merah-tua); }
  #file-input-csv { display: none; }

  .export-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .export-card {
    border: 1.5px solid #E5E7EB; border-radius: 10px; padding: 18px;
    text-align: center; transition: all .15s; cursor: pointer;
  }
  .export-card:hover { border-color: var(--merah); box-shadow: 0 2px 10px rgba(185,28,28,.12); }
  .export-card .icon { font-size: 30px; margin-bottom: 8px; }
  .export-card h4 { font-size: 13.5px; font-weight: 700; margin-bottom: 4px; }
  .export-card p { font-size: 11.5px; color: var(--abu); }

  /* PREVIEW IMPORT */
  #preview-import { display: none; margin-top: 14px; }
  .preview-table-wrap { max-height: 220px; overflow-y: auto; margin-top: 10px; }

  /* TOAST */
  #toast {
    position: fixed; bottom: 24px; right: 24px;
    background: var(--merah-tua); color: var(--putih);
    padding: 12px 20px; border-radius: 10px; font-size: 13.5px; font-weight: 600;
    box-shadow: 0 4px 20px rgba(0,0,0,.3); opacity: 0; pointer-events: none;
    transition: opacity .3s; z-index: 9999;
  }
  #toast.show { opacity: 1; }

  /* EMPTY */
  .empty-state { text-align: center; padding: 36px 20px; color: var(--abu); font-size: 13.5px; }
  .empty-state .icon { font-size: 40px; margin-bottom: 10px; }

  /* PRINT */
  @media print {
    header, .tabs, .search-row, .btn, #toast { display: none !important; }
    body { background: white; }
    .card { box-shadow: none; border: 1px solid #ddd; }
  }

  @media (max-width: 600px) {
    .form-grid { grid-template-columns: 1fr; }
    .form-grid .full { grid-column: 1; }
    .sanksi-panel, .export-grid { grid-template-columns: 1fr; }
    .status-bar { grid-template-columns: 1fr 1fr; }
    .header-text h1 { font-size: 14px; }
    .header-badge { display: none; }
  }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <img class="logo-img" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAfEAAAH2CAYAAABgN7XFAAAKMWlDQ1BJQ0MgUHJvZmlsZQAAeJydlndUU9kWh8+9N71QkhCKlNBraFICSA29SJEuKjEJEErAkAAiNkRUcERRkaYIMijggKNDkbEiioUBUbHrBBlE1HFwFBuWSWStGd+8ee/Nm98f935rn73P3Wfvfda6AJD8gwXCTFgJgAyhWBTh58WIjYtnYAcBDPAAA2wA4HCzs0IW+EYCmQJ82IxsmRP4F726DiD5+yrTP4zBAP+flLlZIjEAUJiM5/L42VwZF8k4PVecJbdPyZi2NE3OMErOIlmCMlaTc/IsW3z2mWUPOfMyhDwZy3PO4mXw5Nwn4405Er6MkWAZF+cI+LkyviZjg3RJhkDGb+SxGXxONgAoktwu5nNTZGwtY5IoMoIt43kA4EjJX/DSL1jMzxPLD8XOzFouEiSniBkmXFOGjZMTi+HPz03ni8XMMA43jSPiMdiZGVkc4XIAZs/8WRR5bRmyIjvYODk4MG0tbb4o1H9d/JuS93aWXoR/7hlEH/jD9ld+mQ0AsKZltdn6h21pFQBd6wFQu/2HzWAvAIqyvnUOfXEeunxeUsTiLGcrq9zcXEsBn2spL+jv+p8Of0NffM9Svt3v5WF485M4knQxQ143bmZ6pkTEyM7icPkM5p+H+B8H/nUeFhH8JL6IL5RFRMumTCBMlrVbyBOIBZlChkD4n5r4D8P+pNm5lona+BHQllgCpSEaQH4eACgqESAJe2Qr0O99C8ZHA/nNi9GZmJ37z4L+fVe4TP7IFiR/jmNHRDK4ElHO7Jr8WgI0IABFQAPqQBvoAxPABLbAEbgAD+ADAkEoiARxYDHgghSQAUQgFxSAtaAYlIKtYCeoBnWgETSDNnAYdIFj4DQ4By6By2AE3AFSMA6egCnwCsxAEISFyBAVUod0IEPIHLKFWJAb5AMFQxFQHJQIJUNCSAIVQOugUqgcqobqoWboW+godBq6AA1Dt6BRaBL6FXoHIzAJpsFasBFsBbNgTzgIjoQXwcnwMjgfLoK3wJVwA3wQ7oRPw5fgEVgKP4GnEYAQETqiizARFsJGQpF4JAkRIauQEqQCaUDakB6kH7mKSJGnyFsUBkVFMVBMlAvKHxWF4qKWoVahNqOqUQdQnag+1FXUKGoK9RFNRmuizdHO6AB0LDoZnYsuRlegm9Ad6LPoEfQ4+hUGg6FjjDGOGH9MHCYVswKzGbMb0445hRnGjGGmsVisOtYc64oNxXKwYmwxtgp7EHsSewU7jn2DI+J0cLY4X1w8TogrxFXgWnAncFdwE7gZvBLeEO+MD8Xz8MvxZfhGfA9+CD+OnyEoE4wJroRIQiphLaGS0EY4S7hLeEEkEvWITsRwooC4hlhJPEQ8TxwlviVRSGYkNimBJCFtIe0nnSLdIr0gk8lGZA9yPFlM3kJuJp8h3ye/UaAqWCoEKPAUVivUKHQqXFF4pohXNFT0VFysmK9YoXhEcUjxqRJeyUiJrcRRWqVUo3RU6YbStDJV2UY5VDlDebNyi/IF5UcULMWI4kPhUYoo+yhnKGNUhKpPZVO51HXURupZ6jgNQzOmBdBSaaW0b2iDtCkVioqdSrRKnkqNynEVKR2hG9ED6On0Mvph+nX6O1UtVU9Vvuom1TbVK6qv1eaoeajx1UrU2tVG1N6pM9R91NPUt6l3qd/TQGmYaYRr5Grs0Tir8XQObY7LHO6ckjmH59zWhDXNNCM0V2ju0xzQnNbS1vLTytKq0jqj9VSbru2hnaq9Q/uE9qQOVcdNR6CzQ+ekzmOGCsOTkc6oZPQxpnQ1df11Jbr1uoO6M3rGelF6hXrtevf0Cfos/ST9Hfq9+lMGOgYhBgUGrQa3DfGGLMMUw12G/YavjYyNYow2GHUZPTJWMw4wzjduNb5rQjZxN1lm0mByzRRjyjJNM91tetkMNrM3SzGrMRsyh80dzAXmu82HLdAWThZCiwaLG0wS05OZw2xljlrSLYMtCy27LJ9ZGVjFW22z6rf6aG1vnW7daH3HhmITaFNo02Pzq62ZLde2xvbaXPJc37mr53bPfW5nbse322N3055qH2K/wb7X/oODo4PIoc1h0tHAMdGx1vEGi8YKY21mnXdCO3k5rXY65vTW2cFZ7HzY+RcXpkuaS4vLo3nG8/jzGueNueq5clzrXaVuDLdEt71uUnddd457g/sDD30PnkeTx4SnqWeq50HPZ17WXiKvDq/XbGf2SvYpb8Tbz7vEe9CH4hPlU+1z31fPN9m31XfKz95vhd8pf7R/kP82/xsBWgHcgOaAqUDHwJWBfUGkoAVB1UEPgs2CRcE9IXBIYMj2kLvzDecL53eFgtCA0O2h98KMw5aFfR+OCQ8Lrwl/GGETURDRv4C6YMmClgWvIr0iyyLvRJlESaJ6oxWjE6Kbo1/HeMeUx0hjrWJXxl6K04gTxHXHY+Oj45vipxf6LNy5cDzBPqE44foi40V5iy4s1licvvj4EsUlnCVHEtGJMYktie85oZwGzvTSgKW1S6e4bO4u7hOeB28Hb5Lvyi/nTyS5JpUnPUp2Td6ePJninlKR8lTAFlQLnqf6p9alvk4LTduf9ik9Jr09A5eRmHFUSBGmCfsytTPzMoezzLOKs6TLnJftXDYlChI1ZUPZi7K7xTTZz9SAxESyXjKa45ZTk/MmNzr3SJ5ynjBvYLnZ8k3LJ/J9879egVrBXdFboFuwtmB0pefK+lXQqqWrelfrry5aPb7Gb82BtYS1aWt/KLQuLC98uS5mXU+RVtGaorH1futbixWKRcU3NrhsqNuI2ijYOLhp7qaqTR9LeCUXS61LK0rfb+ZuvviVzVeVX33akrRlsMyhbM9WzFbh1uvb3LcdKFcuzy8f2x6yvXMHY0fJjpc7l+y8UGFXUbeLsEuyS1oZXNldZVC1tep9dUr1SI1XTXutZu2m2te7ebuv7PHY01anVVda926vYO/Ner/6zgajhop9mH05+x42Rjf2f836urlJo6m06cN+4X7pgYgDfc2Ozc0tmi1lrXCrpHXyYMLBy994f9Pdxmyrb6e3lx4ChySHHn+b+O31w0GHe4+wjrR9Z/hdbQe1o6QT6lzeOdWV0iXtjusePhp4tLfHpafje8vv9x/TPVZzXOV42QnCiaITn07mn5w+lXXq6enk02O9S3rvnIk9c60vvG/wbNDZ8+d8z53p9+w/ed71/LELzheOXmRd7LrkcKlzwH6g4wf7HzoGHQY7hxyHui87Xe4Znjd84or7ldNXva+euxZw7dLI/JHh61HXb95IuCG9ybv56Fb6ree3c27P3FlzF3235J7SvYr7mvcbfjT9sV3qID0+6j068GDBgztj3LEnP2X/9H686CH5YcWEzkTzI9tHxyZ9Jy8/Xvh4/EnWk5mnxT8r/1z7zOTZd794/DIwFTs1/lz0/NOvm1+ov9j/0u5l73TY9P1XGa9mXpe8UX9z4C3rbf+7mHcTM7nvse8rP5h+6PkY9PHup4xPn34D94Tz+6TMXDkAAAAJcEhZcwAALiMAAC4jAXilP3YAAQAASURBVHhe7F0HgBPV1j7pdXujLL1JkaYioKJUxYagKIpiw4oNsYD6rNhQRFApIl2KoiAgAoIdxYpiAem9t63ZJJtN3ncyG5Nsy0w22ZSd+//zFnfv3Ln33HLuad8hkotMAZkCcUWB1nW6NMeACokUOzs07JodV4OTByNTQKaATAGZAjIF4pUCWkqahLGdxOMqfY61yTrr/HgdrzwumQIyBWQKyBSQKRAXFMjQ1p2BgTh9GLiHkZc0SmkzJS4GKQ9CpoBMAZkCMgVkCsQTBXo079smVZG8tBIG7mHkzjRNw/fjadzyWGQKyBSQKSBTQKZATFPgrLrnno0B2CqQvj3M2/cnS+n2c5p06xbTg5Y7L1NApoBMAZkCMgVinQIK0r2HMRwRycB9mfnR7m1797uyy1WKWKeB3H+ZAjIFZArIFJApEIsU+BSddgTBwP+zk+Pd72Jx4HKfZQrIFJApIFNApkBMUqBlSvue6Hg+npJqMPD/pHIzpS69qOMlsno9JleD3GmZAjIFZArIFIgZCrTIaHs9OpuHpyIP9Ips4GJ/Zzmr2QW3xgwh5I7KFJApIFNApoBMgViiQCJlvIz++sZ/i2XQYuudurDzFQwSIxeZAjIFZArIFJApIFMghBSorv1bLCNnG/uaEPZbbkqmgEwBmQIyBWQK1E4KtEjuOAwjD8r+rVQoXAo8eF/qA1W9dk3/roOa1U6qy6OWKSBTQKaATAGZAtWkQLOk1rejCeCfS7d/MwPvbU5ydTeZg2XkzPiLOjc/765qDkN+XaaATAGZAjIFZArUNgoop2PEdqlSNIK+XWaVynVrSrrrQJPWrp2Nz3Ddgn+rWCqXLpEzI3eYKH3KNRcOUdW2GZDHK1MgVigggz3EykzJ/awtFPgVA+2IRxLj5I3cVKenKRn1qZ1Gi//ybu1p+afo7dyTdLK4OBgasif8X6V9CuZ9+R2ZAjIFwkgBZRjblpuWKSBTQCQFNJQ4FlXZ/t1JCgOH3Zv4aaHX08I6jejMMgycP393Qip9Vq8JtUIdqNrd9SUUPiPa4zl1Yfv+50l4T64qU0CmQA1QQNJuroH+yJ+QKVDrKJBCKa+eptMjMXCN1MHrlSp6OC2TLtEbqblaV+Xr20tstCg/n2ZBKrc6GStGcrGfkXX2g/8e/XWq5DflF2QKyBQICwVkJh4WssqNyhQQTYFDqJmFR5JWjDduBqTuO5LS6H5zMsGDze2GXlVxb3aXi94pzKHXTh4lu9MZ8J0K2ivRU+qsvuf2fm7FT4sPiB6lXFGmgEyBsFBAZuJhIavcqEyBqilwTr0LWv1y6Du2f5vwSN6HnfQmWlynAZkUSsmMmNn99IIc+jg/lzZZLcFMFdvJWfWfHMzL8jsyBWQKhI4Ckg+P0H1abkmmQO2kgJZMr9ipcDhGnyaFArxZ09QaugCq87EZdSlFmvDu9ymW2nMQvTb08D7601YEAd0l+TKAJo5BKp9rpVOPShmHXFemgEyB0FFAZuKho6XckkwBMRRYgUqX4FGLqexbx6hS0ZTMbOoLKTxU5Shs499bC+mxE4fJUhKUnZxR3pbguS5UfZLbkSkgU0A8BSTZ4cQ3K9eUKSBTwJcC7bO6Xoj/PoWnv1QGzjdtDWze4zLqhZSBc/+y4Bg3yJhI49LrkZo916VPG19GrtGRed4V3a6tK/11+Q2ZAjIFqkOBIPZsdT4nvytToPZRIFvb+PED9j3PYuQcwC3p4swhYYMSk2lCWl1SBfJcqyZp10AiX5SfQ2sL88gJ9XoQpah1vXPu2nLol3lBvCu/IlNApkAQFJCZeBBEk1+RKSCBAitR92I8ksBb3FIy7N9dTWZ6KTmTUiAxh7swrFsOVOr3nTxCXxXkBvu5XA2lvVNMJ58MtgH5PZkCMgXEU0Bm4uJpJdeUKSCVAj/ghXOlSN+8IVn6TlGraUFWQ4C36IJxOJPaz//q8/dPwk7+g72InoCd/LTD4ZbKJcrlbFz/Ek+/oDsivyhTQKaAKApIUu2JalGuJFOgllMgg5o8DBLY8HSVxsAFNLUBCck0NZ3hU2uWgfO0MbNOhdR/hd7s7oMBznTolNQZZbVBHzyFret0vkfqy3J9mQIyBcRTQPLuFN+0XFOmQO2jQENNkxf2Fe9+HCOXhL7GG5EZ+IjUDHokMQ0vR8fWZKl8WsFpeufUcXcYWhDF3jStw0O7Tm6aEsS78isyBWQKBKCALInLS0SmQAgo0PfMaxLQzF4w8CekMnD+fKpGQw+lZdGoKGLg3K90hnVFn25ISiVkQwuGUlow8LeI9PMHdh+SHEwD8jsyBWQKVE6BoHalTFCZAjIFvBToUPfsezcd/pWZdz0WqMXSxiN9N9Rq6f2MbGCfa0XBp4ptP1T1hAG5aCFQ3ibknqIDxciSKt1OzmL8DjwtQ9UvuR2ZAjIFJBw4MrFkCsgUqJACc/DboXgku4+rlAq6JymD7oKUmwb41Fgouxw2GnH8MP0FlLcgw9CskMpnEllHxMJ45T7KFIh2CsTGyRHtVJT7VyspUE9RdzIGfqNUBs5aaRPU1I+nZtHjyekxw8B5kpsiU9qMrGx6PK1OsOAwejDwO+vrmj9VKxeNPGiZAiGmgGjVX4i/KzcnUyBmKXB+074d1+9a+y0GYMYjaQ8xA+9pSqIHkOP7XL1BauhWVNFsZuFpmpF3mnZbIVxLL+4kKj3b9e/z1d+rOBGMXGQKyBQIggKSDqAg2pdfkSkQVxTokHXOlZuO/vIhBlV18u4yo/bYv881mmhqWj3KVAnQ6UH5e0cJRXlMx0ocNOTYPvoXjDzIsRShGWOUDEnuhkyBmKOAzMRjbsrkDkeQAvPx7WvxSEpewpvMBPCWIeYkGpOSSQZpwnsEhyvu04Vg37cd20/fW/Av6Q5v/JHTUGh8hisNmybkIlNApoAECshMXAKx5Kq1mgJfYfQX4JHswJYEBj4dduTztfErcOa6nPR5UQE9A8jWXEjnQYSUM8obZ3gbWKtXmTx4mQISKSA7tkkkmFy9dlGgc3Z3Rh7LwdNDKgPnrGCXm5NpVlaDuGbgvCKS4F0/GNnQJmXUp1RgvjN0rMTCl6MBeCw92196lcR35eoyBWotBSTvtFpLKXngtY4CdZT1nzriPMiJPNj+LWmvMBO7NTmNxiZnuF8N0l4cczRnIpXgf0YCd/2jvByMO6iRF59R76wR/x76bXrMEUDusEyBGqaApIOphvsmf06mQCQpsAYf74VHsv27sU5HFxkT6ImkdDLFSPx3qAldAPX6S7knaFVBHh1z2INVr7PXOuPPy0WmgEyBSiggq9PlpSFTwIcCZ2adOwj/uQlPb6kMnJupr9XR+8g+9iLSh9ZWBs50MOPywilUF9RpQPWRyCWIwur1c/B8NaD79ZyHXS4yBWQKVEABWRKXl4VMgVIK1Ne3GHHQuv01/CcAScSrz1l1zhtpaGIyXWdOoc5afXBK5Didid/tVrrhyD4qQDKVINKasj7e1r5+l5F/Hvx5apySSB6WTIGgKSAz8aBJJ78YTxRIpJRX8+j0gxiTZLFRqVTSk0hechcYuKzaKr8q+JCx4JmFbGgvnjgSdDa0DHWDl4479j8XT+tOHotMgepSQGbi1aWg/H5MU6Bb836ZG3Z8vhaDaItHUvgYM+x2AG+ZgbzbWci7rRYvvMc0zYLtvAMvjs87SZ8gkco+my0YbQWHoe3CIydRCXYS5PfijgKy4BB3UyoPSCwFWqW2uwsMfCPzYqkMnG+/Z+iN9F56PcoG+prMwANTnT0ERyem0uKsRtRarw/mysOXrOZ49jVLa89JZ+QiU6DWU0CWxGv9Eqi1BJiHkV+HRyOWAp7Nwjbwx6E+HwQP9PoqTTASpdhPxmU9puMBAMIsseTRqyePBovyZlNTyisOOv1sXBJJHpRMAZEUkCVxkYSSq8UHBS5o1vtMjOQbPEOkMHAevQLMWwe1+SuZ9WgEEpjUkxl4UIuCPdXqQ3txH2j4alZ9N02DAIfRgYE/kUiZzwTVCfklmQJxQgFZEo+TiZSHEZgCnep17/f7oR8+Rk0T8+TAb3hrcOVBSSl0BxhPB40W0rek16V8qtbVnV2YSx8iG9omqyUYrQbbyff17nD57V9s+pShceUiU6BWUUA+iWrVdNfewbZJaXf35tN/TwAFJKOvMXxqJ50R8KnZlIo84HIJPQVOIfzs5qMHaKMNjDwI4HX0qOjcVr2u/Wnrl5+GvndyizIFopcCMhOP3rmRexY6CnyHprrhkcSBeXOkInnJnDoNqRNivxVBIYiGbhDx3hJnQ5uYc5zm5+dSTklxMChvxaDRD3guindayeOTKeChgGwTl9dC3FKgZWKHOzG4HXi6S2XgbKPNgNp8UkY2ddLIDLwmFokJJoongPL2NpKoJMJmHoSdnJ0UOdPc1zXRX/kbMgWigQIyE4+GWZD7EHIKdKjTYfS2vE1vo+GmeCStc2Ye1yenAj41m3ohjExWV4V8eqpssJfeANNFQ7o+KTUYRs5zzRnnCs5p3GNwzfZc/ppMgZqngHw+1TzN5S+GnwI78YnGUpk3+7qplAq6BczjBUiEcok8BUacPEzL8nPccK1BFHvj5DZjunc8d8KCr2cF1UAQ35RfkSlQoxSQmXiNklv+WDgp0P/Mq3Wr/vr4n1LpW9LaZvTzBjotTYMqt7VaR1rp+bDDObRa27YF2dCm5p+mD8HI99uDQnlzgnjb8LSutUSUBx7XFJB00MU1JeTBxTQF6lKThw/T7ocxiHp4RK9rrqgD9vl5RjO9mFqHGsIWK5foo8DfDhvdc+wg7bZZ3WFoQYjVfzU2t5q9p2DrG9E3OrlHMgWCp4Dowy74T8hvyhQILwWSKG1cLp0cia9I5sBaMPBbk9LoOeT+dsrSd3gnqpqtbym20Wzgri/KO0XFziDYOFFx8+R2z+zI+fvlanZFfl2mQNRQQJLDT9T0Wu6ITAFQ4KIWl6bgxzEwcJbAJTFwRl9Tg4G/nFmfnk7JIJd8nY36NdUaeclfScmi0el1iGP3g5gyDRj4WBOlTr32gmGpUT9guYMyBURQIIh9IKJVuYpMgTBToFvziwZu2PH1THwmEY/ky2g7JOBYULcJpYIVSH45zGOTm6+aAmzkPgmF+qBDu2kn1OtBFBbjT1553o0tl3///ukg3pdfkSkQNRSQmXjUTIXcEbEUSKes507QUVafJ4h9h+vxYjcBce1sg4EmptWjjFpi//ZVPMfTht8HO/mDSKDys6XAvQyCULCfzNQ2ff2YfdcrUtaRXFemQDRRIJ72dDTRVe5L+CjwBZq+KBjpWwMV7Jx6jekirSF8vYuiloXNzaxNQYedDpoANLTLjUl0AWLf46UcB1zrB8Be52xoJcGFoSHNuX4RkfWmeKGJPI7aRQFZk1i75jtmR9utUc8b0fn9eHpKZeDMzIzIlDUV8Km1hYHzRH+NhCKLkO6z88Ed1PvgLlptKaQuAFIJQmKN2nWTAc3KPUhKM61OA/ccB1HgS2Hl3ORbe3W4vH8Q78uvyBSIKAVkSTyi5Jc/LoYC7bM6P/bn0Y1jUVd07m9Pu+xwfgs8z29LTKFmSB1aO4qLZhfm0Usnj1BBCSf5EspTGXVphDk5LjOw8UG2A3jrb+SeoGV5OcHmKM87p9lF9/+y8+u5tWOdyKOMBwrITDweZjG+xwBVJ12DR7KYxZJZN4OJJqfXo0Rw89qQPpSl7M+sBXQ/MoLZnM7/pG4Vxv82YGSvMpjJCfV6PG58nuE8gMPce+IwbSgqJIvPBUbCFilpU6/z45sPbRwv4R25qkyBiFEgHvdyxIgpfzjkFNiIFjvgEW324QXN4WNZGg0tyGpArYC+xr+LJxVyVVTOw0jP3PMvOfDTYyJmLPjWBiOtAx4528drAy3+hdPb0KP76UgxJzbz0kLkCmUH+H/xtBVZX64mUyBiFBB9OEash/KHax0FsqgJZx87IZWBM6GYgfcwJdJ0MPAzwMC51Aam5Vkkb5w+TsXg3r4+Xow7vqXIQq/nn6o11GDo3OmZDSgNl7kg9A58LrbBc/KMjE4jat0GlAccUxSQmXhMTVf8d7aZudmzR2k3Zx9LwyN6fbK0zQAgI1IzaF5GPeqMQ7w2MW8e/+dwZFsBR7aKCjPyt08dp+lAPLPXAsrw3HcGOMxCXObuxZrgtRFESf33+O9vnlH3bA5nlItMgaikQFArOypHIncqHijAKswWUpi3Z9B8SHPqynEpmbXC9l12snkj9z661y1xu6oItWJNxcu45AwzJcXDehE9hruOH6RVcPZzBBeGxt6BP+E5T/QH5YoyBWqIAqIlnRrqj/yZWkiBC5r2OgvDPiqZgYNzMVNqodPTNw1b0Mu1lIErwZieOn2MtoGB+xfe3mW2OOo+Dcev6cgMpsK/a8st/h1cXHiNNMNa4TUjceDsVNm1dI3Wwh0qDzmaKVBb9nA0z0Gt7puRUp+20KknQAQtHknrUQ/s87YALpmD9KGpiBeujYXVxq/lnaS3Th0rB3ai12spOUlJR46WhyblzG31tVr6oE4jqq+oPbTbjTC0e04com3WIrLCez+Isi+Z6s3OoUPPBPGu/IpMgZBTQJbEQ05SuUGxFEiilHFg4E+hPnugiWbgXJEZ+ENpWfQZnJdqKwNnOu8FU1pRkEts8y4rhT8z2kirPlZSehrHx/uTl8PP9lhtdNORvbQfaG61pTQFVsDazIbutcMIfkGUhmDgT6QrGrwWxLvyKzIFQk4BmYmHnKRyg4Eo0LPVpU1Q50AunebsY5IQWPjcPd9kppkIl3rQnEIlwR3EgboY9X9n9nMQDPwmhFFxEhAvC+e/qKhVCyMNGWSlju2KaO0nOkpPYahZf4mbo8j/tVrpqsN7aCtCsoJiaVFPKf8OMp14zfDaeQkZ7FS4DAYxbvUJ135eu6cv7nTlhTFGArm7cUYBmYnH2YRG+3B6tOrT96utn61HP+uW4yoiOn+OzkRTMrLpQsQ91ybv87Kk2QUGPvTYQdptt5WjWutWelr9MVHjhvw3F3U4s4h+/Zbof48mgGGVl8qPIpb6ruOH4d1eQLbgHL9EzFx0VeG1M8SYSN81aA6TDOzk0rvHZ2fSmt+XL+p/7rVyPLl0+slvhIgCQazdEH1ZbqY2UmA+Bn0tHmm5v/FCmlpDF0ICH5ucSUm11P7NC4bznu8rcdCQw3tpHxi4/0VGQSajljb/rKKG2UVuBu5b7MVqevZlM02YbCGrVQBBKVtuTEmjZ0FjIUVK7TgejsKcMBbJYb4uzKfTDgcQ7SQXJuYyPIMlvym/IFOgmhSQJfFqElB+PTAF+p15ZRsNKT9BzeuCYeDshPUavIvfTq1bqxk4U5oZ+L1HD1bAwJnlKunK/nowcHZkK8+gtRoHvfR0Ht19q7HSLOoLck8hlvw0ORW152jIUqqxturQ06lZUK8HdXFh9cZAFRn5kioXmQI1SoGgVmyN9lD+WExToGPWucP+OPrTVAxCL1W041CgPqYEuhsJTLpqg1J5xjTtfDvPG5U9q68/sq9CBs6uBWP/Z6YxDxeQUsGCYeXF5VLTky+Y6ZU3EFNO5SVyZt9GXJzmI23rORqettpR+NqzwV5E7+aepHWQyjneXqLJhqvnda7b5amNh39mwCK5yBQIOwVkJh52EtfeD7RJPfORzaf+eo55glQqMAO/NTmNnkzOIEMtUetWRqNisJKnoe79FF7op2C/LqtCZxl81H2J9NIzRaTV2NFMYNZjt2vo+Ekj9bjEQbv2surdX4nMB0OiWk3vAfHsTCCfJdYiydwK5v3A6SP0GbKhlff6F7WSi/qdM+Cmz39ZBs8EucgUCC8FZCYeXvrW5tZXYvAX45EUhMxSIONdX2g0A30ti/S1iHlUtFgOw147D8xkIpg4A6L7s2claTRKeuBuPY19ykp6HQOLBWbgwneErG7bd2powBAN/budgWL4XX8/dwXUy/3NSfQcLlN1EJ5VW5TsVmRDe+z0UfoCEnmOo4RTqEjdy3wr+hGPjPImlXJyfUkUqC17UhJR5MrBU6BLows5behePJdIZeD81fpA1FpepyG9Bft3bWbgfLv+GVjoFx7cRROR1KQi1S57mo+8V0+vvVAIBs6x3lIYDbNwJ7VsZqOvVlrpuTEez3Xv3HNrTqeLVuISce6BnfQxYEtry62f195bsJMvQihjfR3jEEkufLZ2x/Pbuc0vukXy2/ILMgVEUqC27EmR5JCrVYcCzRPa3L8jf/M4tCEJvIW/yekyLwOe953JqXQ27LBS2FF1+hxt7/KGzHGW0LO5J2gN1Oc58JYuX5BatJWRls5XuJ3YDPrqgrUoyFGipKkzzfT4/6xk+c9z3X8WOD/72XoDvZZWlxpCKq8Nc8T6il+KbdCEnKAvS+3kQayZ4lYZnUZtPf77W0G8K78iU6BKCshMXF4gIaFAOmW8coKOSwZv4Y9r4UQ1GghadwKAozarhvbBce1rm4Vm5Z6m7baiCu2x7IHOQC5rEdCUXa8Q1AsdK3XB8vHXPwZ68nk1fbqGs6GVD7biA6OhTkdXJyTTwwlptWa+GE5nFjLAvXLiiDvVaxClpHFym9f35GweHcS78isyBSqlgMzE5cURCgpsRCMdWKAW25hn4bUD9vktiSl0Q2lWraCOR7EfjdJ6POYcMImbDu+j38HE3cXP/i1QS4X4+JEj9HTDYCd1bG91q8NDW/g7Ctp/UEu33KOmb3+wkgP24NIO/fcpdjrkib4Zjoc3JaRQi1pgK2eJnMt8MPI3EYZ3sBRkR+J65erb8bQK7bzJrdVmCshMvDbPfjXHfnadblf+emTDQjTDmJ6S1hKrz9vpDPQ+7N8ZsD9KPAyr2fPIvy4Qy0X/FNtpcWEuzcg5WUWaTBUyb6lo8ngD3X0bS8jhp5YLeDxff2ekSwfbyWZ14IsVq+xVmMerIJW/ARW7x3Ic/t5Fbv543o67SujGI/vpb4SjueAzEMR47X07XzF87cYV8yI3EvnL8UIBSQdvvAxaHkdIKMD2vTvxSPb6McG2eo7BRBPT67kZeG0ovhstF8lH/gZW+SpLPn0ApzFLSQlk6rKswPOGgi7olkBLFziQkcwGaby69m/x1HZB3j6do6enXtDRlBn5eLG8VM6t8YUsBREFr6TVoXO1BsrwQdQLgsGJ72AEax6H9/oDyIb2a1EhFWL+giglqVR39ik6PDyId+VXZAr8RwGZicuLQRIF+ra/ps7aPz9iBn4VHknwqZxqwqhS0v9w2N9Uqj6X9PEYrsxwqSfhsLbSUkBL4LD2K35WzeCUlJKspYmvaqlXDxvVr1seI71myKGg/EKWyg00crSTdu5hdX/Fanw+TNrrTTQsMZl6GcyUFefwuDzeOZZcGgs7eWEJX8MkX1lcWjJ9emn3K8d+8sPCn2tmPuWvxBsFZCYebzMaxvF0b9b3sh92rv0An2DwFslrp585kW6GDbW3zghYT8mvh3Fk4WuaR7mx2EqL8nPpF1shbWO8c5z1HDJWeVHQwMtN9OgDDuraxe6O6K4JFXpVVGCpfNsOLU2eTjRpWvn85J532V7OU9sQADE3Yq5H4OEimb2Fb0pC2rIS87gOfgxz8k/T2gI2dQRVbJeee12fz376gBMDyUWmgCQK1I6TVBJJ5MoVUaBr0wtu/XHXdxPxtwSpFGK7aTejiWYh97dJOu+X+rmI1vc4QJ2C1L0Ocd4brIX0KRh4IVTogSRvjvseeIWORo+0UrvWxWRgT4OoYn8KsgOldeY8E8LRXLTpb9YOsFResWSuxrwnIPLgPEMC3ZGUQl0AnSuAzMRfKcSobj62n360FAaL8lZwUccrhn/9xwq+JMtFpoBoCshMXDSpanXFNRh9bzyS0NeYYnU0WpoE2/eZCEtKgnNWPBc7pLINCA37AQ5PK6Ay32dHYBJL3QEGbTZp6OLeOnp2jItaAHxFp605u3dw86Gko8c1tH6Djia8U0Lf/+RBe6u4NT5kkgHh2gaRCA8kpNIF+BmPJQcOb38it/tI2MoPAx43iMLG9e/xXBjEu/IrtZQCMhOvpRMvZtgXtLi4x/rta54AE+qL+qI90NyBSvgfA2yib2Vm0yWwk8ZzYbTyTVCZz4dKdTEc1crDo/qOXgjj4v/Xa9XUo7uWht+spMFXFeD3kVebi58n4eg4cVJDHy830FNjbXTqNHDd3d7aFY+D32BMgCFJqXQ71OyNVWo4VcTfEbQGednvQa53O7QxIIfU4tKRYe0VFw56/qNv5jNDl4tMgSopEH87SJ7wkFCgmaHV3TuLtk5AY5LTWHnCjoYnplIH2EbjtRzFIc1xw5sgfX8FT3M+sAMlzFAomG2paOh1Orp1KNFF50MlrXDgd0F5OEcBaVk9Dg0LMqO99a4OqnZIo38j9KqK8bA3u7BGkqgx8sTfk5gufZFFwcir6sJ3MKV8gNDBZfk5VBIcOExx8/T2Y3ac+HN8lA9V7l6EKSAz8QhPQJR+nhM3dGLBSUr/3DImEmbcmJRGLyZnukX3eFtgnApjPQ7or2Hrfh+gHxbYun2Lv+DlDRMz6jV0wflqunaAhoZcbSUdsM6VKuFdoVaogVukzFz16rLTm2ekNruaZsxV0nQ8f/zpsZlXTBXP2BnO9aGUDLralEh1kNtbuvBavf6H421BF+Gih04foyVYJ0GkNeVusU5+D56W4eij3GZ8UCDeztj4mJXIjuILfL4HHknhY7yQ6mm1ND6jPnWDA5Mmzth3LuKCvwPjnguV+Q9wXhJ3KCsoM11Hl18CqfvGEjq/K8OkcokHNlXVIlXAZq6lFat09A682Tf9xW5fVWsacPejVkh+cylCD68DM88GClw8lDysm9+Bvf7I8YN0yG4PZub5dseIiOfEAz3kMYSeAjITDz1NY7LFthnnXP/P8V/+h84zJKQ0+zdeaIIDeBYYeAs4snF+rHgpLqh9P4RadBHUor8A2MNt8S3Hg/3HiyArat5MT08/pkSiEged1dGT4zvembfvrAupTsmlovkf6ui+R4spLx82cz/iVSChg971ABzTz5hALyCLGIdwxUPZDnCfqw7vpVwktAnS8+GvFmkdJ2w/+ceseKCHPIbQUSB+TtvQ0aTWtZROdUefoMPPYuCsPpe0JpRwVBqD5CW3m5Nh15T0alTS2c16cMr+47DTb/AuXwwv8z+hPreVUZv7d57vPCoy6pV081AN9ThPRVf2LyajoRQHPSpHWrOdKrCY3E5wL77mpBnzIJHCk5vcUK4VM2mPR/tjqVlux8i6cJLkC1Uss3QLej8DPhSvnjyKFK9BmU9s6Zqmj50o3jWpZmdP/lo0UyD2T91opm6U961nq8syvtq6ci662QePZPW5Dgz81Yx6NBBSU7x4GXN42DSozBlOk6UmLpWrzgVP86aNtXQTHNVuGWqjRg09oUVCvm65CBRguznTyulU0p69KnpzspoWLyumo8c8WorylGIHOC5Z0O7cgCQ5lwKq9wy1Lqavirw6ZhacdjNyvhgGcSnh28/Ky7pc/czKnz/+Q15fMgVkJl6718BmDJ+dZiQFcPOiaQPp6KGUNLpMb455CjKrPQ5P83FwQloNL/PTFebw9h0m4GPhqNaqpZ5G3uukli2cdO5Z0Sd1FztUZLMpyWwKKmY5zPOqoHVfm2juIjUt+9RKeQXMzKu+9LDNfChC064G8l8qMAeCYIBhHpP45lciDO11rLdtVk5yKrnwKzvxtJD8pvxC3FFAZuJxN6WBBwQWBFgRy1OoKTn7GMNqnmMw0lygryXFSfax+bB5jzlx2B0KVDUcqkDbfr2M9Mj9aurTswhSoQeYJYijOPBUVavGH3+bwSDV9MzonGq1E76XhfC0TX/pad4iJb3xDsfKV83IWTpPRHz5vKxsOgvJVmK18MG731FMI05yEhUo2oOz/Vs1lDCtmPIfilU6yP2uPgVkJl59GsZYC0okL3HegU5Lsn/zQkkC6tYrQF+7AsktYnnhMOtgZfeX8Da///ghSN5VSaqspFBSw2wN3T5MQ089mucGDo0F6PdLBpnp868g5R4ogTQefZcM/42joJxcLd16rw4Sup0KCzmYjzXH5Zk6rz1m5pcjBerteLpo9DFrL+dZWV6UTw9hHRZDvR4IZ6CCw6ZYTaaZDiq8O8YOIrm7IaKAaC/kEH1PbiZCFOjatO/Z+PRaHIq82RmBRRIfZgY+Dgz8yhhn4Ez+r+GwNvDYPrr16P4ADFxBrVro6fWxRlq7jOh/jxWAecQCAxcYYk6uYM/fuz8WAHdc7lSrS+Zb6KuVahpyjRmZ2yq+ZzLjY63JCkQMDMMc3n7qMB0siXao2oo3Pm/CAcCWfx2+JW2QGCiIogEDv0NH5g8vPWtgzyDel1+JcQpIOshjfKy1tvtnZna+5a9jG98BARh9TfTFzSPxDEBqyWHwPudc0dEuz1U1yQ4EI48CrvXXSAN6nKXvCgcjOKspFVp67209MM2LqF6dSKUBDWbJsp5ASWu+SKT+V+egARfddZuZpr5ReQrRYL5SE+/8tdkIFbuG5i6wQEJlqbxyONeWej3dmpRONyLGXBmDi5RXXT4k8VtPHAAOAdLUBjeGwos6XdH/699XfFcT8yN/IzooIDPx6JiHcPZiNRrnG7ok9DXuEKss++JQnIH4b1YqB3euhHNo4trmRb4KqvN7IbVxkpKqvM2z6+ogBarppWfgrq9mmzerc2Np5OgxslSnNlBQboGQMvS8c8306Yd2SLpsNoixsTjVbk3Ci+OVNHMuw7lWbPpgXw0VZitDo6aFWQ2oFbzYY2mknpVcgsU6HLjrawvzglGtczM86UvwANRXLrWBAjITj+9Z3oThtcUj2vucgUr4/xsDfW1qRjY1U2vJGAsG4ArmkRf3Xkjcd8B5aBeyS1lKBNQw7+EuSN38nNVRQ9cOhE32RjtlpHnCnvhvsRYmpqA//zHRub3sZLXxOHh0Wtr2u5qaNymKOSbumVZHiYqOHNXSS+PV9OESG5087VGfC5cs34OMM6Z1Q9TE7Uh/2h3ogcJ8x85RZ8FF81es1zFYt3uKMYd88ZR2TvFC/+Oyswb3XvnbYhhV5BLPFBCtWo1nIsTb2DrXO/96jInxz9tJYeBMBw1Uzg2RNvR1Th+K5CWxyMD5uLbDdj0Z8bh3A+7yb8CkFoKBl1fGKshk1NAToxJo4QwnPfZgPhg4CzIe6TvWGLjArD5eDnHM5rURMwt4/S1WxEhkBRHfGJ4Zc5Fa5aDsehaaPD6fFs3S0A2DE+Bc6GXM3prkDhFchYiD+zD338P/IS9I3XSkhs97rofe4LaT8170xMtL6A9f2juDgR8+74w+V0t4T64agxSInetpDBI3El1Op6wnTtDRp/Ftyd5MaoC33JeaQaPNqeSMYemb2fVEALaMB6BGxapzBWk0KrroPD2Nuh8hY70tbo/z2GNy5VeY1aalCy9V08+/+UrdajqzjZ5+/66IVKpYzZbmO1bkfCtR05QZOnpzqpN277GVIqCVv6QwAzwbDmNz6zUkswu+DpHYlNX85lM5x2hOzsmgs6HV0Td57oh194vV7Ib8epRSQGbiUToxQXZrF95rgEcS+ppbfsNhd1tyOo1Nzog5ec2XVoxR/R68lufnnqwkl7OC0lKQnAN43l3PtmLcgso5Xkpevp6SGwKfG45gyclJlJ2dTX///TeGp6Q5U8x00/WchCV+0OScLj0985KWxr7GjnuVe6hzHvMn0rPobmNyTF5Q38g/RYvyTtHB4JKoMGGO46kXL+tcHoeXArF4MZXnrwwFujXq3QS/4pO6oRQG7rEItwQS1qr6TWkMvHtjTeHqS4o/i610w9EDYOCc+rHsMmFrv4ruud1E365WU9dzCsHAYzMsqfINoKC3piEBTaknd8+ePenqqz3aVCdNmsZvetOGxsNG4kvYE6Ms9PNXerqsnxbmEb6/ela2d4QOLIjXTh6jwScOws4cS9EGwhgeTkilxXUaUwvs1fKjCziTTJQ6eLZd3n2IzMgDkiu2KsiSeGzNV0W9fRu/ZPAWzt0oaT41QFzLVKtoSd0m1AAoWLFaWBX+BxKWDDuyj04UI1NWuYEoKCXFQHOnKunSflbYGD3hSrE64or77YQn990j9TR9DiOfEa1Zs4YaNWpEHTt2JCvgPTMz9HTwX6hpVIEhTmOVMgs/SqJb7rWR3c5e7BWbDhppdfRRvcZUF9CtsSbFHCgppgHudW6n4uBs/SCMeQFRwS2xOsdyv/0pEGtrWJ4/fwpw7PddeCShr3ETPPEvZtajnxq0iGkGzmPZCgY+HOFjx4uFNI9lS8tmKlq7VE2XXWwBA688c1ZsLy4FrYU0+t5cQcps0qSJ+2nZsiX17dvX/bvjx+004R11TGtbAs3RkGuAfb9PRZdfbIKmRUi6Urbstduo+75t9ErOCSC9BWoxuv7eAHnWf85uTmMz60u7sXuHgct+wU0mSpt27YW3JkfX6OTeBEMBmYkHQ7UIv3Newz6XoAucAIHR1ySJ0Ozoc4HJTOOBPX2DMTaBMXzJ/yOyjg1Anma2FZZ1TNMjScnUCSn0y9dahJAxXGosepuLX2y/bASDLpXOWrRoQc2bN3e/3L9/f/dPvuD8+ruS8vNFRxyK/3iU1OQ5NuoLaTEuM9+uSqK6ddi/s/wxV+x00dSc43T2gR3Q4sSOep3nUIU5Hoq9y3v4fOzlIO4hykI6eeeH38za1fPMS6+LkqmTuxEkBYKY/yC/JL8WEgp0b9C70w/7v/gcjaXhkTx/Z2HTv5denzKRn1nyyyEZQega2YrD99ZjB2gfJCucyT5FSTqdCjCpZthLhaQa8GcO3YejsiUFte9uor82s1d6CX311Vd04YUXunu6d+9e6t69Ox0+fIRZAG37TU0tmglAMPFblO7kKht+1tGCxezJDvCUCnJ4q3CpbQz1+kupdegs2JuNbuk9Ngov+aNOB92BULrfEEYZZDk1uM9tZy9eN3N3kO/Lr0WYArF+jkeYfDX++aX44uV4JEvfBnjnng/c83GpWZRZav+OVSc2toGvR/zvKCSNYAbuX8DAtRp6+nE9GHge/hSro5S2tjb8bKLLriuh06eLcYFR08mTJ8lo9GJxd+jQgf766y80qgQanZlGj8wvDauT9p1YrM0wtLPnG+ntd4k2bvLgAJTRyoCZD0AylTfT6iA2MzaORU8vjwE3frWtkF44cYQswSVRgY1J8S32Su9YnN/a3ufYuXbW4pnq22ZQCoa/Bs8VUhk4ky0VCFZTM7NpFuBTM8DAYz4iGgO4H9JHeQbuRj2nt1/X05hR+bWGgfMcb9+JpCc5grf9mDFj/Bg4/+79998v3UFO+vnXEtApNhhVKLY9q9hvHVpIS953UbMmfLGpwJxQmlDlTlwMba7YMLt49jHv6ZuMSTQF6YH1uKwHAfEAocDVE+gJawZfdEujUNBcbqPmKCAz8ZqjdVBf6lCn2+1rNy85jJfZO0mSMZNjv7tCfT4ZDLyP3hTU96PtJT64XkbM7EmgcpUtajj9vP6iCdCpBXFv//aOHWpjF8aNBLMcWqZWK6hZs2blaGM2m6lu3bru33/5TQkkUsmp5KNtKUjsj4saNbDQ1yut9O5EA+zm5RP5cRrQdQW5NPL0USoEI4+1a05vvZGmg5Gfa4SdXDonB8Zhcb/FX8/edlaTi26RSFy5egQpIDPxCBI/0KdbJbd5ZNORDVNQT3LqULb13ZqcRvMzGtD5MZ59zJdODHrxzqlj5PCzbyrAvFQ07gUTjRxRSCplbEhSgeZfzN8ZtuXNKQbaup3VxC7SI5vX0KHlc1+wp3qfPn3cTeYVOOhUTqyxKDHUCFTHBehWRDLcXEAv/M9AZnP5nEB8SVyWl0P3nToSbAhXoE6E9e+9wMjnI+fB5aakYOBauW/a33Z/PT2RsibecOGtkoSGsA5MbrxSCshMPHoXx59bcza/iu5x/LfowjfwOhoNPQXb99jkzJjEPq9ssJwzmnNIs8Tkb+nW0MvPGOihe9kDPT5jwCtfAAr6d5uT7MXCxeXiiy+utGq/fv1K/+ak/41lll87tz+r10eOyKdD/6rp/K6sXmc6eGnBHv6fY53djbS1sRaCxvvCAOe8qcBd5zMgE2dBEFK5Oo+O3rfgm1n/iD545IoRo0Dt3MURI3fgD7P3OWoxRCInL5E8P62RMOHTek3orsRU98fixa2LndkeQlan7XBoKzumVs20NORqR6kKPV5GHHitcI2du7Q0630hvK5Bgwb04IMPVvqiJ16cKxw95qQ//pQMry+uUzFQiy97ZnMRrUOymPPONbjR/HyDPThSb3VBHt157BCdcsZeZAPrWe7GGfB+nYZ0RnBJVPjsaYVn3zUX3nhmDExpre2iZCZRaylVAwNvZmx7H8LHNuBT6X4niohv6+DQ0gaqtDfhvFZPKcl5XUTrka/yE5j330jPWBakqmljoG+976D69WIn1jeU1Dx4WEHFDkEKb9OmDZ1//vmVNp+cnEyDBw92/33PPjut+6p2b3+WyHXaInr/PQe9O0lHSYn+Si/W93A2tOdzj7lt5LFY2iGv+lScCXcgJwKb2IIoDT765v3fOmafOyaId+VXaoACtXsX1wCBxX5CS4ZxOy3/vIH6ksUjZuCjkdzhK9y6edPGW2E5aDyAOXLLOLOp4ZX79OM6atcaiUziRucgbfYmvMNSuIBCN2TIkCpf1iJHfLt27ZDJjJ3hnPTBUheVOCsGQ5HWi1iu7aLGDWw0fFghvTeJbeReMzDrdNh0szg3h760Ae0vOJjTiBOnBc6EZ5PSaGRaFvFZEUTR/HHgp7HZ5sbTh/W7rU0Q78uvhJECQV3Nwtif2tr0Xgy8vt8JIoISPHkdIH0PSkiiO8zJ+K94ZGUu+hUJKwYd3E2cxMJb4IXdJIG2/85pROMtkYmIyceoDx/VUH/kN9n0t5CJ7c8//3Qz6UCF0dx27twJW6kKqGZmOq8re/PHnso40Dil/V1Bx0/qaMD1agDEcEY0f8m7LgBhZkOiPVOrl9ZslNWeWXCaZuWdpl3AV/Cg+0nsIqMJeQEIJL4sVw89BYK6loW+G7WzxS7Z53fDyBkpKVsKA2fmzaqxzggbW1CnAQ03p7iTS8ajNZh9rqdUkEuZbZijR/K1pfYynx271GDgwvgHDhzoxkkXU848UzBxsjS+ZEXtpZ8/rVyUkWanlYvt1KuHGX/yx10/AqY3GdnxKkqvI4bm0VLnNpwVS+s0os7Isc4QzEFIcRybuDeBstjpVi5RQAGZiUdsEpSv/3xg/Vf4PIMrSJoHAyBTWxuMNAtJEJIhTcVzOQRYyc8tDNziKXzsqOmaAWYaeLkQVlUbC0OKPvUC23CF8XMMOKvLxZQ77riDNPBa5vLhEhedOCkpAELMJ2K0jpNSkuy0cKaNWjZjXuXjsY7/Wl6QQydi0Mmt7GSk4/yYmVWfnk6vQ3yWBFEa5tPRh9WU8F4Q78qvhJgCQVzEQtyD2tncXAybDZiSTk+WvvmZBOZ9hTt5SdlQq/giJrOnh04dpo8Rt8uqP4FdAZNNoaVD21SUlcFqz+go4yYm0anTJRXkMQ9X/4BMN81KFiun3HTR0aNHKSMjQ/THevToQevXr0d9Nd073ERmU81I5B7fqgfvLkJykpr5pmii/FdRQRMmJ9KoJy2YT6avtwwD9sIrKVnSm4yyN/jgd8fEF+XTQ8cOIibeWSb/gKgOw6MiYcHAi655etHXs2TsdVEkC30lmYmHnqaVttg+s+uVfx77cTYqJOGRJH1zo/3NSXQd8J37Qo0e7xPH41tlLaA7j+wvZwt/5P5EGvd8IWy60WML/+NvM02dQfTurJpLLAK3NPdRzCAuS5YsQcgUq4HFlSeffJJefvlld+Wy4VXiWgiuVq8L9XTLUCUNHQw7vCJ6Pb5dLjXd96ieJr8n5Gb3FA0cw76p34Qax4kDKTNyu1JB9yKV7yqE1AVRuIminu0vHfLVn5+tCOJ9+ZVqUiDeeUE1yRO61zvX7XrBxsM/cgITDuCWRHe2XfUyJdJEJGdICU79FbqB1FBLbOEfDHz073Gw+CrMlRj/9t/0yJXNHunRJcnZixUAUTHRa5M4FI4ZVLhV/UL7U6dOpTvvvFPSzPz444/uzGZCkbQcJX3H0z7n9u56jpE+nlsICbwmaBNEN/1eUdA//+rozK5sBff2l/fi5XAknZZW1+2HEi/ldEkJPQiUui8Lsd+C0/DlJVHW27l09Ml4oUmsjCN+VmF0U3weunctHnFGS5+xpKg19EpGXTd0am1h4Dz8b6wWGn5sPxXicPEWBT32YAK98hx7pEcnMpsL6umPPtHTO9NV9MvvUHdbvHnO2fmMc3tzvHYoS+fOnalp06aSmuQsZ5yuNJSlsLCQdu3aRS+88ILfnDVqYEIooJIu7mVHPH/NaSqqOzZHiZpuvENPHyzxeqvzgZmA0MZZyEfQHZEh4b6mVXcMUt7Pgb3/W+AxPAWkulOO4mDU61CNqT5BKlwBjEAuNUKB+EMFqRGyifvIha36N/9m66ppqN0Dj2hau29WuPGbVCqagbCWbnF2WIih3h7kCi8qw8DZAtGtC2fgih41etmxcN8GX1VI11yloomTTfTwE04c9MJFZOnSpcSMbt68eZLs12LoJbVOWloaXXPNNVJfq7L+Qw89RJMmTeLFW/oo6cr+evpkQTGWs/cyE9KPhrExtcpJbVu7N+N/X2GmnQf4370lxeTRY4SxCzXadDK0XFfCVJeZXp+GHT8gXKClSeU440oGodO5Zze+4JZf93zHmke5hJkCsiQeJgI3Szzjvp15/45D8xxYKonOjHXcD+rzB5LTqZMm/sBbApFcgYOj48GddLRYiH8WipLO6Wykb1bayGDwdzYK1F6k/u5waBDLraPh96tp7ZdwkkKAEqvYMzMzafTo0cRMLx7Khg0b3ElX9u/fTyXui5eaGtTXw8tbSZ3a28hoiFU0PQXl5Wvp/It19Ndmf3txEySa+b6uNO1HLM31UUjlsxFTPunU8WDjyfOaJrW/f1fun+zEK5cwUkAScwljP+Kt6VkYEKeSEu197pkINRj4UKArPZuSAei2+Iz9rmyyPR6zr+adpLeQqYzRsrxFTYvn6BFaVuhmhLFReP4U8FpX00+/aum6Wx1UUCBIpHqkwmzbtq1bOs/OZpiA2CtWq5XuvfdeWrZsGZ0+neMeAKPBPfmIhoYh9qJpE+ESxvCmsVl4/pQ0d2EC3XKPMD5PYTPXT9nNyAxbf7wWO0b/9Olj9D7i44O0k2MB6JEk1/pIvNIoGsYVvyswctTlzD/D8Ihm4MJJp6CGOj2NQ/jYy2Dg2lrGwD3Txcf9Xkjg/gycqOOZWiCLxYYE7l16zMKdlJZip/59LbR8oZquuJhBNtRktdrpt99+c9vI2Uvc6ZdaNXKLV+yXV6xY4YZ5nT17Nhj4abymprM6mmjamyZ6dowdaHrseMg5uWOVgXspUb8ej8Ff3smFSn0u4sbjufAZNDYlk15EPDmfTUFkQ4MPkJUz8vwVz3SK9NhkJh6iGejb/AqO7zmBh61okunaFJmGZgGAYQjiv+PJ61UqebcAYnVFQW6515o3VVDdrNizq3oGwszsogsKadkiGz36oAke2uzjCA/ofzYTh3uNGDGCtmzZIpVcNV7/8OHDNGvWLBowYAAtX44UYBiDQqFxg+989pGTbruJIVxjn3H7XsSyMkowX7UTY16N2bwFKG98NmVA+yDRMshkZF+gtnjyGxtb3VfjC7YWfFAys6kFNJE8xEzKfnrtjhUn8aLk8DEt4k6fhPf5okykDFTpYkZRLJlIIl9ghyF/CBslVLRaeukZRpaKFTV6xYN1K9cVxfTKszm0CPbiC88zkVot+DtOmzbNnQs81B7jIskuqtoPP/xA1113Hd1+++2l9ZXUoZ2Jpr5hpA9m5cEhiqMG4ouB83jObFNInc7kefJFcHPRPnhwF8X4mhQz8bzr+GxaUrcRPZFRh/jMklhYjWHeY9k6vnFCKzkETSLxAlWXPBuBGqxNf7+sw+BEJSnnHKMD/8O4BdFKQuHKo5FZ6H5TMmUjbKXWF5wWc/JzyvFqNeyszUrtq/FCowu6W+mrT230wF0GXFKEUR04cIBuuOEGevjhh6NKvc7OahMnTqSePXuWoryBnQEg5NyzDLRumYPuuLUA/x1dMfuhXidl+Ra7a8yDrfiQw9f5MtRfja72muGMuh+Jlm5FnnKVtKPOMxDtnvytz+M//h103vUs8MglBBSQxHRC8L24aaLPGZc1Wffvyj/4holH0mWIid4OYWPDAeF4rSGhFtzlA08704Sl8OuBHLXHJ8MSQFZp/ItGemhEvEl5XpocPa6nflep4QHNIDFC+BxL5aNGjXKjsUWy7Nu3jy655BL6999/S7uhglOehlZ+qEaiEH80s0j2M9zf/udfI7XrynPjZdpsI/42uyk1ixP0NrE05L16zFVCQ4Gm+A/wHILQj/Erlqt73Zb08Zcz4/v2J5ao1agniflU4ztx9qpiIhj47xhUQjAMvIfJTEuQ+3uwzMB91oWLtsOhbbeNGZn3WDAY1dTmjDhbPmWGk5Vho/Vrimn2FCMlJQoKnTVr1tCVV15Jb775Ju3eXfOw1Cx9Dxs2jDp06ODDwJU05mE9HdhMYOAcJSCX2kgB3p0ZSLzEGRTPNZrd2dAkFn7BBAZ+FN7rjKMhl2pQQGbiEomnIjUy97hG4DXGPxe9enmhJ8H+OQb279fS65EpjkNTJJL0v+rHKsgQlZKkpn69YzXOWCwlXJRgttNNQwrphadM1DCbsfFV8GC3uVXrnHVs+/bt5HDUDMgN2+UZXe7999+n3Nw8d1+yMpH29r1EMPFiSkvl+QhC/hJLjpiqV3uP0HQw8kkZ9Wg0vNeNsAkFwczT4L1+eyJlIOuAXIKlQO1dgRIpdknbAR3xylcl5LgNPyXl72Mip4CBT83IpgdgU2qglO3fZcnvxCXnmROHJc5KPFXnmIQSuv/OXPrl62K66vIEt9qay5dffkmtWrWiW265xUcqDv3YOe77scceczuvffrpp+4PsOPdg/ea6euVLhpyTR4uGwJgjVwYzMxFnyELWG0uDYDy9gB8eiYgNJaFFNFSjZdoqjw6zmdqQf+zrhpQm2kZ7NiDoHmwn4rd985teP7Qn/at59uidOc1d/KSBJqd2YBUfuAlsUuPcPTchZXYau9WKvCDWiXAdibSJwsF7Or48nyujIrClmSQkbVfqWnQUAUVuvHXBa9vTiH69ddfh2MK6P7776d33nmntG0FtW9rAOPW0OiRrDpn+jPzrp0MvCKbOBPqYmQWnA1o5NpJFe8y5PE74ex4zeG99HNRYbAob8WXdB149eofl8rZ0CTscFkSD0ysmaUMnANFJV162PHlmsRkmgr1uczAAxO6ohrXDhIySEkifHCfipK3BEbJUnm/nsWQylV0cR/Df31r2bJl2PrZunVr0gGvgItOq6U1SxQ0ZmS+G6teuEDVdlZVnvT+4ZBhm5qob5j3p8rpolm40NwCh90sd0y55KIBA/8Eb22Q/GYtfkFm4lVP/rf4M6OviQYw58WMCyklQ7W0oF5jejElS7Z/i9hgHyEForUcalntYd0Vk8hFiK6jTX96HXiHDx8ugprBVWEI1fT0dPfL7KskJFuTGXdw1Kydb3ESlReTM+kdMHM9/s0MRuIu5lfOxbO+dlJQ+qhlJl4Bzfq1vewS/JrhU8/HI83+jdOPcZUXwvv8QqQPjWdsZenLrfI39trtFWQHd1+J3IdAbWUlufkqOnJMYOKMtV6/fv1Qkr1cW3379nX/zmorprHjmPISj+Cw9k5uPFYowGlal9RrREkaTTAOb7zozsNjOSO140OxMuZI9VNm4mUob6bkVz//Z+Uy/LqN1BOMvTOfAaLRj9ktqIOGk5fJJXgKKADwoqUWzTzq9NrHxtkufuNwHr/glc5IaeFm4v369ftvyjZuYmYu6Q4b/HTH6JvyFafyieuIM/CX7OZ0f1pmMIycGzb8e+qPV9vUPeuRu6+4PzlGl0jYuy0zcR8SG0g3r4ByOOMOO7BJKiwvsi1oGDw1TZLelCtXTAEFdeqgoi6dBae22iiLnzyppLwCb1jZoEGDwr5YLrroImrWrJmb3qvXFdGWbWyPl1lV5YSXaVPVojRi7TyYkIqzMZ3qaDiliuSi3Xz4t1enrnjrC8lv1pIXZCaOib603aAM/DhSRDZOHyqZJm2RW3gSEgSMTRKyj8lFpkAoKLAACUWOHBVishmONS0NYbVhLnXq1CmV9tllq4QeHsNfZ2lcXtdlSc+Oq1eaOWGRXKqiAKdUfhFM/IOsBtQaavYgVhKfyZ3x/N05u8tDMrX9KSCZYcUbAdOp7ujP/l5yAOPKknpSKQGo3Agp+qYjfOxqZB9zewPJRaZACCjAjPPHX9jDV2AR55xzDplMNaPjeeaZZ/4bwaHDDtq3X8Y1qGxK20O6lEtgCnC8RUvQajriya9KTAHWflCsp+3GAz+/Xk/TcHzgL9aeGkFRMl7IoyXj+BN0+AWMR/JO1GMRvga0ok/qNKLGKo18Gw/5onDRocMu2n9Icmh+yHtS8w0iItulpqXLhdhwlo5vvvlmSd04fvw4XX755W6QmF9++UXSu127dqWbbrrJ/c62nXb6e7NsF5dEQLlyhRRgRt4EZ+WbaXVpHM5ObXBCj+pQ8b6H6mobTL/94rsY9rrWl1rJxC/uMJDRuJfZycIJ6yWJGSxrp8Pj8mFkH7sB0ncdhFHUhpLrctIpJD04hTCwCh/+G57qFH89hot++MlC334vpIBkJ6/aUviwe2+ujuwOgZ5JSUkI90oWNXxGEWPAlt69e9Nnn33mhmu96qqr3EzZZhMHX2swGKhevXql33PRlBlBxfyK6m+sVCosDAqNLFaGV6P95Gv5UJydo9LquM/SIPSXysP2/cNnrJm29ZqLbmZTaK0ukhhYPFCqd+tLzlyzaen3GAtnH5O8fs7Wm2gOgP9TcIuMR1sYI6cxWf4qttKqgjz3lPOvFhTk0qkSR6Vj9gQj3Z2U7ma5XPoAqa4Twuzc+GMBiHWB0UTv5J4gm4xq56b4nr1w5wN4Bpdnn31W1Nbbtm2bOy/5hAkT/OofPnyY5s+f78ZeX7hwoai2+Juvvvqqu+6uPU73JYoBaGpree4V1or450qv6lrpLN1HTK+vgGD2K7J9iXHO5NceSPH3rVHG2Z7wHAUPJCTTTUC8u/nYAfq1CBnx8AeJZ2rdj76es//cVr2H/7T1i/dr69qUzMRinFB8ut2NR1L8Fzuw8IbtCabE+OfGGCeCwJg924WxuIC0VJADFS7RYjDrbXYrleA/HGUODzEbzHdBqUE3FZ4mQP+6PiGFOoOhn6X1kF5ozYPFVhns6vvTzXTD4KLS/vofonEwDRUO4bc/9HRuL6ISp52ysjLcEnWnTp2qHO67775LL7zwAh08eBD1BEe0QVfoqWEDJ02ebid7sYAEp1YriesyDntVhRk+e6r/8MNP7vCgGW/r6ZahtSf1aFnaXDbYTJ+tteLXQrQA0+QxaOPuh+e1wMxdtBlZ+L63WSgf2qq3Th//rwneR7yfxBadj72YZ/JRfIe/wc+tZtiTffauwPaEXSf+C2J7UjP1GNR3Qs4x+hBnz0lO8gNaSRwLT8qPeC6omR5H11dqkyQ+F6S/Ho/kMSchQ8//UrOor8EcFwxc2PAK2uKw0QmobN/MO0E/WQS8Y4mbp9xq9n2/GO3xswWJNZ6xHqZsrY4aQH12PZLANNfoqB2eQMaIqTOVYOJ85agN0Ks4nl1Keme6DgycE2u4KDs7u0oGzuryGTNmuKXv4mJOTqKg7Lp6uqiHhia+aqHU5GKqXyeR5iwqgW3b4pbGH330UXdSFZa069atW+GJxIlPLr30UjDxH91rYuceNTlKlKRW1Y6LlJcoCsrLV1OOWynlvzt47W4tsdGeYge9l3+SjuAnp9KtLkMti1z43HEhMRALEyuRcEWBbiQDUOo+XCBS2LkWduZYLuyu+RRQ3trpjPTEiUOUh/wJvumIRYyNz/TuGtKtubLHoFc//nbhlyLeiZsqcS+Jn9f4oj7f7/n6Q8xYEh5JhlW+bdcH43k9vS71gAQZD2ykGKPY5bDTm7knaW1hPhWVQp2K3zSVLZnA7F/QMArv8//2NSXSwynp1AyHkAGpWbse2kn7y9ht69Y10sEtzJxKSvG742bvVXABUlJRkYZ6Xa6mn34T8nUvWLCAhgwZUuGg169f7844xupypqher6IG9fW0dL6T2p5R5MN0FJSTq6Zb7jHSss+4XVaLu6h9+/buNKd33303qXBRLVu2bNlCXbp0ocLCQkybjo7vUlBaSm1KQ8qXRyV98Y2J+g4QLlWewuu3NSJT9sHEVFiatEf8Hgp+DTMj9y31wcw7g/lpgfX8eEqmW8WYFqN+OjyyH6EF/KgwlxbmniKnBO2FD01s55/R+5b1/36xKHgqx9abcc3EO2effefGA7++iSnhtS1prKwG7gMmE08ZirYU2+hjYJRPBQN3lsMpF7NwmYQVKTJYOgvOXsqhJlfBLnYX1O2cT/wmZEHyLUmJOvryUzV1bs9MKb6lQGYYn6420pVDBLVthw4d3BJzSkqKH02YWUyaNImeeuopN4PlokCAxQtPGeiJR8BwS1W+ZWc0v0BH/3tBA6m8GEzd6+T23HPP0fXXX0/Nmzcvtwg4Nv306dNoE97yC/R05aWWuL9MeYngy8QF/5BoLirspcYwXY1MzqBroDVkoSPw1To6R3Tz8QP0BYSMIBm54/w2vR9cv/mLydE5utD2ShJjC+2nw97aJHzhTjyik5cIhyFRNuIZr4XK956kNDIGFwYR9sGJ+YBncr+HU81HllxaU1hAuSUs1YIdltvdvktBSFtgNivpsn5CfZZC6tZR0sh7y7sT/LNFQXPc6UKFRk+eUtO6rz095N/5Ml//DyvwHSZxIiRBvjiddKuEvYW9Eca/aKSRIzzIbWJGHpt1mIm/+LqR/jdWGCunBp04caLfYNatW0ezZ892S+jCalXSWZ00NG+aGjC1NtJoqtJYsDVVgbnR07g37fjpcdZyuVHaXnzxRbriiiuIvdM95aOPPqJrr73W/Z2eF2jByEsoKcF/jmKT2mJ6LTDx3lcm0Fff5oh4oexxKsyPp2SkKalXD9CO9eFlCs/Lt+vVwMkv+7eKLscVs2bWHHLR4GcmzFYddQa6zZRC3aAxcMbYOWZBNMzYnONuRn4AvgZBXEZ4cW/D01rExMV0lXhl4p9jVi7i9SxldpgYqVj8i5C8pK1aEu+X8pkaqcuLPh8bYYOtiO4/dhB5ur3wnRV1QKFQIf2kkjLStTQQ6twbrysmPUhwZltftay4rhcgHGfLViH0fv0GDU2Y7KDTuVA7AkLUJRlCVUlNGhpp5yY7mD3n1Y7fwgAvbboY6N9tAhPfsWMHNW3a1D3gnJwc+vzzz9346R7pW6fTUId2Zvr0g0LMGzNWsUedggoKNfTEcwZ6/wMb5sarIh8xYgQ9/fTTlJEhRO5s2LDBHa5mtXIdFf3zk5batOL+1YbCTFxFZ1+op42bAjv18R7ikpqsIaNRRd27aGjU/VizCuYnSjKbnNS6ZWXmCAVt3aGD/b2U6WMqc/Hv2+7lFl1kt7vo2Am8i98zkp7YkqRSUzsgSs7KaIBsinxljq3yD7SHg4/sddvJg5DKeUP81ch4xuy9ln8nxNbIxfc21ua0ypG1SGwzeHve5ndRCfBpEu3feCETEvgiQAO2hMNVLBdeuZ/AAWZm3in6vchSyeLnqcf9Hz90Wg29/KyJ6td10jVXCQzEq4gTyxjKUsyztARp5pv1evrjLyU9+6KV8i3FpeFTQh+qLuxMpSHLUTVp1ILqOF7Lp6tNNOweXHhO24FopSCLxQLJWkMnT54kTkzyxx9//Dd0rUZN0yaa6eYbCipVnweiEzOo3zcZ6OKrHHQKjFywsAjOdHPnzqUePXq4kbUGDBhAK1ascG+pl5/R0uiRgvNW/BcFrfkSc3JnscBAyxXvHtLA6/+lZ5LgW1BM/fs6qWVzvnD67iPPy1Wt9/LHsQB5S3T0qIoWLcW5hIv5i+OKKbegmEpKcCX+T6VW+V7iv3QxmunqhCS6zpREmkBbLsom9pdSO/kC2MmlePn7DMOWrWvx5AHb9rhEeosbJq4nzdtWKuZky5IhvjzZx4YjfKMCTVeULekALA/20jcLc+i1E0eqWPCCbfve2w2UXd9Jj4/kkBlmkOHe3Qhncxlp7kJIHduV9OYUGyQ8liAD2boVNPiqBPpwtr9zUUxNjIjOjnnOTK9MEOaBVdtjxoyhJ598kl5++eXSt9n0oKK+PU302UeQi5Vsp63+nDldJpo6Q0v3wZ6OeIL/2uzZsyetXLmS9uzZQ23acFI/5BnoBw9pdhMNwXdFkCTCVZT0wmtGevrFikw5LNWqafjNOmrfTkX3Di+poT3EpjD251bQp6vUtOEXhsUlWviR1UdCr3hNsLmKHXXnA/q0WYxpGvnEGocIgIknjwUjkfM6ctTXNX2tb4/eU2evnb4vwgsrpJ+PFyb+LajSzc2ZJBQefCMs6qtxO30QGchiHZPpEFTmD546BOm7iIo4TKMCWpjNaup5nomefKyEOp5pJ61WYKCVOUNJIKeoqt5kGgra+IcWTEtD638sKk30UXkTF51vpmULbZQYp/bY3DwttT5XDU9zC3wRzPTYY4/RqlWr6LfffoMqVTAjZKTpaPIbOjqvq53qZDlCNmc8JzakHN30t5YeekxJP7o944XMcZ07d6aBAwe6UeCOHDlCyUlqmj2ldji4WW06atFZQQcO+qrAFW5V+QXd9PQcksOc2a6YDHpBvV3ze0jYLxwC9/dmHcwjJXBYdNKf/1RsAnNb6MHIG+PMewURN+cgVWiQ0Kei9nqoKxVCC7HNUUwPHD9IuxDKF8T11W0nH9rvzk7zP383btRJMc3E+7S8JHvdttU/YGLq8/oUu2h4IfPAuwK85Q3EfzeMcexzKxb3n3D+eOzkIdqGmOzyBWhbGHPzpiYa87CCbh2aK5ZUNVJvw89mhD8paccuS2msekU2PzUtX6SnKy6JRwc3Bf273UhtzrHhYHK4IVbZJs0x4GyHZlXtg/ea6LqBxXR2p/CaFA4c1tGHSww09jUr7PAckFjivlSkpqbSvn0swCigUk+E9qZyL/gaWTRh/gg7mk15L4FGPOKv/UlK1NO7E3V07cDo2kMecpw4paFPPjXSaxNdiO0vImcJQzmVT+XL58E9yCz2EJx3zQjvjKWyD865t504SFshrLCdPAhmvqtpQqvZu/K3ct6MmC8xy8RTKWPUKTr+PGZAcsJjDsUYlpQKtKUUqhPjQAms/nermYAQ5QIzLx9aqYBXuYGGDVHS2P8Vw77MUl0Qyz6sS53t5mqEP8HR6sMS2ru/onAyJZ3f1UjfrrbWmMQT1iH7NM6S8O33GWjW+2VNGpi7LBPdd5cKly92rGLWEsj0EIpeKxBPbqI33lbStz+UNWEoKCXZQCf3sBe8OCz2UPSo5ttQ0n2PGgG84+/QdsfNZvgiRHuYHSfQUdEL44z09rtOOnGSL4dloz6EqJCBicl0B87B9pDKY6kcgdZxUv4pmusOlw3qPCtJovT3cukEI3jGdIlVJj4TVOfc35Kyj/FgDQhlehs2ob56c0C0sGifWVaYjzp1hJbm5biR0coXFV11mZ6eelRBZ3WMBQlWQf9sgRQxSQFmXgTHHV+JXAEnLxV9skBHl/YNrzRa0/N+OldHA67X0Hc/eJg4a4pUNPQ6Ez3/RDE1aSQ9QsA7Bs8Wl3rQKajQAu/qp/S0cpWdDhwWHLVYEjcZtfTDWg21bxvYY7umaRma7ylo3wEdtTqb4LPh0WwpMF4drVtWUhoJEJovhbcVBZ3K0cIHRUcjx/Aa4giVsiGe8AIGOt8MOPSeB1hkqaskvP2vunU+HT4AMMzTJ49Uaj4M0D9e0Jt7tb3kmS//Wb0kkmOpzrdjSo9yfvPeQJSmPXiGSWXgTKRsxEs+n1GXLokDBs7BWi/lnKCP8k5XyMBVCC15dkwiLZxZDAbusXFWZ6nUxLsuatvaQrOmWKGyTQDT9nVxgCwBWMv7HoFy0MXoeTG1dKsk3sY/4Bfwg0eqhfNRXQM9PdpMc6YUgYGLS5xR8QegEp6RAIYkKdKytCkXmLWdprxhoYWzdNSsqRGOdALNLUUOWrGqJtZD5L5x8JAaDNyr9dBqVcCO14GBVx2qGbkeV/RlF8LdbHT/nYW06XsDNW5YPh89M+1cQPEOP7qfvrdzjoLYKey3fwP8mT6v35TOA2BUEH3nBd0ODHzGVRfeyJktY7IEMe7IjLNH8x6Xfbvj2w/wdc4/IrrfXJHtPz2NCTQtvR6ZELrjm/4jMqOp3leZgb8CBj4FqiSXH/Ka23UFoB9A5nrUTsNu8KhfY+l+zbQRpnfBYjVNnami7zZ4PNiheAakZP4hMyBGObRKfLxsYIqzSr/iZSWE24WLhgpqfU4ivPUtpNOpEPetpiXzbVSvjodZBP/dA4d0dNVQBXVsp4MdtxDhYsEwIIEmrPK/b5SeZs8vJovNQV06Y15WK3HRQvx+jaj4A89g6GooqHOPBPr9Tw9ErYqefsxAzz7BTC6Uay50Pa66JWEO9x1Q0cChWvprc7H7QuwHI8sAMYBwnZGZTW3h+KYTf8TW1CAq/Q7vTws0kXcDd/17ZIyrzKk3QEftbeqdPXLzoV9jDuVNNDOM8EytxPf74ZHkfc59ros425sTU93oa7EWH1kRzRVYrA+dPkKLIYFXhLp2VkcTrV7ioPTU+HC+zMvX0yVX62jDz0I4FSuaH3nQRK8+F9oD1VGigTMXx+F6qd6xPdGAy9gGXz4NZWj2g5I4Y9klVzvJUqik1UvVdH43trcGw2zL9+j1SUn02NOQ5HFAb9uopOZAdKvOZYS1H9t3IiPdbWowOAsVHDbCMzv+fBT+/AdzMojo8FGeByc1bWyk1R87qEWz6tEvNGumeq24gH+1ZLmRrr+9CIy8PHgSh6F1MZhoHpi5McYc3njr/gJtwt3wXj9SGtEhkVp8Q/sGT2+J70W0eizoJDl87GKpDJyl7zQw8DfS69MDibHPwPm2ZYPj2jg4cyzJy62AgStx2Bho0UwHpaXGj8NRQoId8eElkFDZf1FIwjhnvotOnQ5GRVzhtQghOTp64DENPfeKhZ5D5i/Pc9t9dup4HsJxJiS4He8kKIBEbGpB8t+4SUk9uhvo568JDDx44Bb/DwK+Fl7Ki3CZc3sm4+L38BNCXvfqFL7MtGxmh4kGueIvQhjc/9gZqiYc7cT2WtCyBV+E95cs1yLkUYiXhycGTRpHccHAmS58QRx0ZT69NU4PbRa7FPmzAPb2/gnS7BhAnp5CLoPqUDP4eQjuTe7rubDrv5FWj9Jx9pdNFiOiVdbQs8n254vaXnKTiPpRUSVq56ilse1d2yz/vAkqMXyapH5yHuvWBiO9mlaHOsYYqEFlq4LtVW9gY3HK0PLwg0rq1iWB5kwtphZN4xMS88gxPQ0drgOGNTtTAYTjKSM9+Uh1wnyEJbXwo0Qa9WQxpC6++FSsKtWotfTog8A0fywfULShVKciBvmQFrHXBEjOUEUNCAh502cl0l0jmT6CM5rZDAnsfS31vchjY68OQ2fvZw3iyoHPfWY0OBkKY56zIMGN2T/x1aLSbGvSzlgBw0BJ9c/Q0uEjbH5Q0kP3JNEzowviDp+AxzoZIXSTpzto89byTq/MAHsgAdQUnKHJMZgVjeFalwG1chqidoqD8153dGrc/cHf9/wQ9ep1ScxR2pYIvnZzU/PndhTuAJSCNOxz/iKrgwYgbOKd1Druw6s6R1XwIwjtmxuLrXQPVEQH3CoixEX+NyhWLgNbvLEO6j6i5lD3xabNLjC9+JDet18L1bMa9mMbJHMdJEIHndEiOBUnS9Y//aKniwc6KA8Qlh5wk/L3RSY2SytKmvCSHvHaoVXjC9/jJ1QSLaPi6SgpWwl8dP90pDdel0hzpwlOjtW1Y/N8hNdXIPCa8NTgvny/wYy1YYdHvQPofkb6YBbU/BKx9pmx/fiznvoNclBBgZ2MkFQLDjM0sRRcevH9jmxNQRNUUKChiwfpMG5G6/PGk3t8iS4FVOs0SLZRySiqIKDn5L8Xnusr8nPIEVxaUybIFjztIjtXVX89GtXpe8DAn5LKwBnA5Qz2Pk+vQ2+CgcdyGj7vlLnoNzDwIUjPedCOWE8GNvBh4Bo4onw4x0R/bWB7HdtSQyklRteyZabTqIGVNn5jp2ULjLRtuwNx1cHleOdDf+1XJuozoBgMnH0HhPzaQmHmxNh9rD73bA/eyw569GkbPfU8q9bL594Onlr83VAxcO6Fgl55Qw1mxuPyvcK6aPlKK236KzTxwMIlIPJXZJ7LeYuM1AeY/8KYHfTRsny6Z5Q2KBPIhp8RWodLXaJZCwdDVsmGSkMS/AoJz5uC02uC2U5fLLdTv16s8PSua/eqxGGzEuGro08fdXchlhi5cP4raGJaXfquQQtqhSQwnixvEujJBwDjDR8e3Ou2qE2oETVMfMBZQ9JArD14GvqcnqLpXR/JS+Yg1vEW4J/HOnyqZ8NscsDDHKEfBe4MPr6kQPZohLxMeFlDVw8oIKOhtqSGRGJ4g4Mu719Ab72uh+o0GBuogj7/IoGuvsmKQ9/Xd6DUs7+pgebPMCIhjJGy6/pbchyOEpoEtMZjxyWnpxe9jqtbsaBQC5AW2MIrkDzywZzmLlIBxjVqtn01h6ug5Z8l0r2jigEb63UG5LHbrNgwEu8YBw6y/wMjnCmoUwcj9evNmox4Ly63c+LiecXAX+AQNP+1wSRcVpBLP0CYkEzQKCAdX8UbIdx2TmZDagcTq740TFJC1/hgqLP4y5k7GhnbPC7hvRqrGhW7OYFSXlj226IjTG+pFz69SkkPpGXSB0gfyvCpsXRbrGqWN8AGPuzwPjpdJr82v6PXaen1FwAJeQerdqNDIqqpFcvjZY3DbTfm0ktPu+jHX7y5r8X0wWbXwnGtxK0u9RYF7NI6mjU5gX5cZ6Prr86lxx/KpS8RE3F+1wSfek68Z6UJ77DKWh11seoslS76WEcnkQXNc+D6Jp9kgMoJ7xQgTWxopHEx9A5PHcEm/8GSRBp+fxFSs/p7WRv1Grp9GCOSSdsb8z900vGTVup2jp4+nlcdgJ3wjDqcrSaYirH+rcgZn+A20fmWfAgRnM74V9iZY7U0BCNfk9WQRqVlBcPIedjZey2bX0ygrLeijQYRZeIDu1yfbiTdvHw6zfZvyeFjTMxXEfs9JiGNmsQ4/rnvwvgdqfduP3aATgDs37+wqldDM9/RA4qT4TBDqYaNtqUZqD8uurh3Hg5c8Y5VrAYfdqcB9j9fqYIZuJbWLiN3Ws/0VK9E17ypnaYDPa5sGTfRRkVWSWCBgQYTgr8raPsOLWBC2TTgSWpDdKHJ5JPkguWqEnjh8+di97rLkvInK03uMKkTJ8uqu7FDtEo671wPwpx40v76e7Gbgd13pxpY8fxviaK8+E9FZc3MDDutW26jSy82Y+w+qnVoNo7AnDcYZr3vrLHrOMvr5j5zMo0GI3fnz5C+BVT5dJQzvBcO6HotJ9yKihIxJt6rxSVnLv154R8WsjF8qiQjIxO/rd5ILwJ9bZAxkZz4Rbxstx8hgd8KFXouJPCyY2K4y9df1NHggaEGOomKtRhEJ8RKWkD5hgR+z0gDLV6WC7r6xmEDU/4pDVDtPKAlZaheYW5aDtsKorthfuXTNTrkbPeqgBMAp3k9cLEfSs30Y9nrvrEhPl1y0EeYey+ueT6IV6wyA2uek+WUdzhjzcNjD7ItW0qsvQJx73rkDlfSLTfqkdyEk7v4+kmI61vs12InPjucH610ATIdlrWR2yCRj4Bw8QdU69L5X3RQh9fPzWDk32Y3pQ46UzDjYJ5pXPbjh58M7DG0ezSMKiJM3Az1+ZfbV68DATj7mOj14LZagmFfmpBM72dl062wfzP3F91ANFC8kj7wNeQHMPC7oLY6Bgm8rIzNKUQnjdPRwyMKkcSkNh4w1Zs8BZgxp9H0eoN72nPS/MVEx47xSirLmV20/0BFWyT6VtyJk2qaPMOfcXU1mmkAIIaHApqyDlC4PL0uKCiB3Vzntv3GVhHCyIbeYaXTOZU7nGWk86ik3bK271RT21ZGemqUg9Tq+HUQDTTfbK5KTS4GNoONhl7rbyNnip5A4pHbjh6glVa+6MRm4Z3QFKHHs5BD40LAtabgshtEyVz67fxvwJGWB/FuSF+JABNXTSyg06MxikwpI2HmzfHf9yVn0CspWZSlDIrwUj5Zo3V/BXrSKMAGniiHosRqHzU9DpSy224UUMvkIpUCLtJqiuGslk83Xw+bn8L36ucCGlwh3XqvpgwmO44o2L3fmlqe3h47c/QcYkpa+bmJdu322ix5vww3JZMLncxCnO/QxBS/2+4339vou+8ZwTgWCl9xVcg7n0APPmaHX4LHzMTmJf8jLD1NS+d0rsjMJNjRP/scNEEInm+EAfsSTJpG9NhDBdS0SWw6cIV2Fl2UlWEDIIyNup4lgCz5lqMQMsacOEx/OmLXRs7jqQM7+cKMeohoquvmLUF4r4MJOS/TkmlhaOkvrbUaY+I9W1/GJ8Za2OTYpiCJA7P6nFWDi+o1pseRAzctBsEHqpqW36Geuv7wHtpn45SB/oUZzkdzk2nMKPlwkba0y9dmFemMt600eiQ7q/lacFy0+gscWL21kMgFJDg+5O940EAr1/pm6lKQTquhFR+YyGiMjvngfjJzGvOsHT8ZYavEfRhdBKCO82BycofaYP+wNN4KIZgM4sEs8dDhYhr/jhJpHHm80XMdqWiOmckuWJxAPQGBm1fgYRxKMGsz3XoTB7V4j7GUZB11OLMi7AAFwE1MdOX1cN66XEe5eV7Ev983GWjoYCMy/lV3hcXX+8mQyO+/B7E+ECJ8C3v/s7DBoa8bYtpGLmDyDTIgrwYco/tgzwSxE5RAJ7gO9DnZLr3z7ZFYATXCxM9q0L3XV1tW7sIAGdJONAP3AA4MgBTxbb2m1A2QekEQORJ0Ff3Nv3GbHXpkH1mQyMSfgSOMDNCBb40z08ArTiPxR+0JIxNNvCAqKkHHZ0fn0QN3wXnHLZELhXOx/7KxgG4AKtyp00Z64jkT4tDzwOS8Uh1Lfe3aGKk/UqFGk810zHM6hL15GReP6hU473j2Ch9ULI1fClug8Dv2Uy+BbbmQ9h5gRl8jx0AQs8U9hZZhtYnuvN9KjhKPDVxBzYBn/vlSJ/31j38Y2LsVOCLyRefF17X0yFMFSG9rp2++L6Bb79EBDEeY/xbNiui2m04Coa02O4qWnx5WrQ+5uoDmTTPg0so+FN51wmdVLmzkNx8/QPuhYo/lwnuiv95EUyCV93NnQ5PMZfiF1L9PbJx0UcfLL6hpWoR999ZXNxr52/4fPsXAWH0u6XssUVydlEoTAN6SEWfSN0tD7MR2Exh4LjZBWShVvV5Nr4010b135JUyDPmACc3mcCLGvoTeBEb6fXckkAr55UvZOH446UvAul55vRLxwvmlDNx7tbrwfBOt/JCRwKLnQnXkqAbgJnYq8blsXAaUrToV7JfbwcRZo+V7cXl5PNh5ieRDKzRTEaAVd8jcR+zEZiOL1WsDb9XCSJ995HRnZbPbeX74EfKc18nyZyhOp4pmzDXRs684yOqOJRf2USGcrK1W4ThKMJdAwyL7mVQ0HUpFCWzj+fTqswZgrfvLX3xmFeLsmpd/mqAHqpE1Ec6PsIg4HjCzVyclUzL2SRC7wvj1H59+gT6uCWc/y7YtiakG0bF3Dzr2voz32LAiiiZu6RtPQzjivACCToT9O5bS4oml0SaEbNwJT0+2L/njcvDokYJzgpbuv4sZuMy8xdJUSj0FFdPEcfl0962ecBovOtv3P5bN4a2kLmcZafHcIsrKjCY7oILmf0i0c7eXwRkAZnEHEv5UdASlICvVMLc07t2K782109FjopVjUkhcjbrCKfDpajPddCfAdU54xocUoQBh+XolEAqb2+nt6WrgtwtzxSFR1w7UUqvmgpaELwAsgU+caqY7H7AQA/UIJ4sSsf9GOG5ZKT0tei5j1SBWDbzqohF35tPsKUZQ0D8REJ9d7yAt8hOnj4k74Gugt9X5RCouv29BaPygTiNKBCN3h6JJa5DtNH3wfN+1Vc9LpL0aXO2wMPFODbpdiO58i+cWPJLg6thmVw8MfApS4d2K8BiJBAyOCjX4FkvgnC5v6LH9sCvhECmDxKbX64DEBo/iwYyDLjPw8E0NH/wl9OrzFnriEQa48M2K5hu6pqALuplp5WKFXwx5+PolvuXjJ7XuTGW+ceEdgUrVSVP5lrsPDL6BzufvsKP/8FOoM7SJH0NFNZkBf7rGBAZug4bBw8CVyKDGmOgwDWQiegMS9t+b+W3PBlJQe+Ri9/3vt6Ym0hOYX09IITP6Phcl0CcLHZSUJDNw8bMk7JXBV+XT9LfMyCHvn/2MbeScGvnJnGNuQ02sFx7tmdhDc2En7812cukob8xXu/+49auP29Y9m+3lYS0hZ+KNDWdc+/v+DR/xIPBIyhfJkHhPA/t8MYjXGUSM/eXgP3c8nu8B5DIcYWSnHGXtSEp3pqnJr+vowXvya3WYS1hXfJnGTUYHspMV0uiHGe3P98ooSG2Z6Tqa9DohvWt05WdnRvfxcgP99rt3l7AK8G4w6apKIvbYXUmeyzEfufAReNlOx09EC3iNAmFkiQByccD5zMNoVdT9XBN9/omDmjcVkNQcDji6fuwzJ7j833idgNzmcKgQQpcIZz8LVOaecDEF9etjQtIcKzKceTABanKlxf63WLV+200F9ObLakpJ8b/4OWDOmZNzkp7Hkwv/kngoXTR6ehd28vuT0kknnZEzCYz/HP51Tudm3QeFkx4hZeLZyoaj9hT9OwMd5pNENIALH5fMwIfA/n0X1H2N4gh9zTN5PEbORvbo8UN0HJ6d/tjWCrrwPCNU6Hq6FWFk0eQ0Fc7FFx1tu2APLabnn7QBsQ237v+c3dwpIKDKtdLTzzthN5Z0Hw370JxOLT091otKxhqsc+Cc01dXddgYjypbpfULp9m81UFffhdpPHhvGNnDT1hKYXGFNKpNGhlo1jsOJMBhU4bAIFas8pW6iXpfqIXzFdToLhXi/s1wYsuDHd1TH2k1u+tp2ps2aFOkI7mFfTJj6AOcj/ze4RZ6EamAy4LBlEAifxfpkt/MPem+aMV64RGwKZcjol4CsFgDxlqQDvOm27jzh0Vo6rdw0SOUTHz9Aee+F9FRs3vnSSgdEArzW8OW9FJyptu6JellCd+JVFVeDMzAhwILfTds4f6F1bXwtIWUMXQwQ6nG/uKPFJ2r8121ykEzJ1vokQc84WferbFijYW69lED4jOU26U6vSUaP4n747+WRqcC5UTE5ukDZn+OkdGqvP7ro59hO7Loe3f1Ol/h2wpavNREPfozkIuX+Z7VSUdrPyFq2dw/pO+7HyBh+ziTnN0Jjjf6Eho3MQEx/775sT37C1nwsqMjLDAMxKvxJgdeYaUz25TX3rBwMh028ifjxEbuIewNxiRaCA1xe520XA2l77ME0BHPoT6dr2wW6smq9qmUqchm2NR9eLq4Ly4ii1tZiVtNI8Suvg/isNNNPBaWL7aU2OgGxFRyNrKyDPzcsxJp1cfFCCcLLi92PNIsMmPi62MxJIw8mDMYEMbX2csJtXUBDblNTzm5kYUrZUZb7DDTC69x/mevR/UAxIE3V4nbfrz3HklM98GOBjLdwSJ4cUdOGuer65at6JmbMQuXC56DG6/TU7MmvkwZJ+FhDb03xwtLrNcrqVFDFb08HohrLwBW1w3HykVNwv6yQ9sS2CGRTRQHDhlp+APJCD9jWsTnmVT9/eWiOnDwXPUxp0Bm7VV5r/V5uafo4VOHsaPiQyjhUTSFhng+MmWea4JfADTHIu7LvqTmxVR33cblfyVSXc4VErJSrVWqIt1Lx1wHpqM32Xgk6RsNCO35H+zfCwB9lxq3DJxoA2zgNx4BFjqnE/Vb0BwSo6E3XnZBDRjbcZYhW41R0JBG46Q3XiykB+40IvzMf3t8+Y2VrhmmR5awSDJythmrwWSEw5G1eyr8z00wRQkK5sBHC7/ZBpfn/nDa8ZSSEie9Nc1JJ04ZIiKR82V39MNF9PhIMy60KtBegTkw4+EEN/42VqdTgQQ03sVSN4vZvpKef9WGWHIP01AiR3YCgHms2GflMdYrWmpHj2mp/9VKXGYK6Oa7+cIm6UiLgtVbk11wUf26dsTq26l9W4Zn9S+sWv8AucgnI/zMvU5rsmth/BZ7ry/LaADelUXG/8JTJX3QkEeHn0uk9FevOGdQK0lvVlI5KCbeq3X/bEzK7BKyPYJ2RYePCYcOfERxi+Hwsbth/2YM23gtm6BCd4eRlYNS5UWtpYmvGqh7F08YWXzcWONhLhkQ5s1X8+g9eOIKB5RwBLHk+8U3eTjoVUiowiApNa9+3r5TC2br9axmlfjAxGS3I6iUkoyL893JaaRVepTqLvoTwCkLPmQVaSSOXPZNsNPLz5ymUfcnuFH13nz1NGLBy3qRK2jaTJaS+eLLe0bpDju7e2QO5sSbkrRbFwMtmFFEGen+aUorp5GS5n2gpr+3sONcCS1ZkYuc8xp8IfoR7aTMe6jrNm5oo08WWCGRs43cu27cHiVg5B/m59ABp2euQv31yLTHCbfuMKXQu5kNYJZi0CjJ+0WTRydGrfhlyY9Xdr8hqbqjkMzEz67b9fwvt6z6FZN0Ez4u+ap6vsFEv8P+fS2kADckZHVHEKXv/4bcu9cDyOUkZyMrM0gtUiVORDKTm6+P3bR+UUr2EHbLCUc3C2LDFTigfNGqECK4sYgatnHRm8g/XtMMb+VqLVDKvKrhBEgGbK/TST9IqJNWTx3hj+I9hFy0ECrSU6ciGzf+9OgCevpxfyQ234ld/ZXDx5TgpDWAzBUYurDRtBo13TpUSakpYsPIcDGYlVDqKOgxUbjoq++K6MY7TNC8SD7mQrgOo70pFzVuaKcvVyhhIy/vVLkHUNLXHt1HOxxiL1PRPl6hf7zSemHvvA9Gfh77l0jffywBJC//YcHWXp0v57jyoItEJq565dfDP36Cr0lCX+MBsv37YkgM72bUp3RIAaqI3PaDppOkF38qBowjpxMFwIQ//1a6UaWmvGFGzuIChJHJanRJhK3xyk7EJlsQI64uPaB4uwhAJHq9E8AiNSthHIG6d9psxsby+laci0txNxwmwRTOsnp3EqRxnwPop19s9PmXkZLGhVHotQ4w4or2hoJWrzPRls3+DKGg0FPXs79MNPxmMdC4DAijoSdfSKBRTyIczY3oJoQWug9qhEotWFyAHPR64pj8aIanDWb+Q/lO/XpFtHqJgtqe4fEl8GivXLTXCqdeZD7b5YbNjZ/CZ3sC9s676fVpMrJq1kX8vHA6SCpZX278dCXkYQ7LDqpIYeJzoGZ6GF/h8DHR/WTmzShST2fUoTeBhJMUZ/CpZan+K1Tojxw/TCcYia2MDZwlhIfv42xknA9cbC7soOZVfikEFBDmyEktmhbSh3McCHUSmJtOp4Ynu44u7VeTmhQFrfvaQFu3C3HSXDjz0s3Aeg5Wm8WbmDGj62u9Xsa8ZqfNIrIX17ypwDtlXqnadxr5t8dOqBE6VpbBCxTQYH+NfcqEpCi8vwKnE3UiccwHHyfCIS4fMKzMYISQNr3Oo0Lndh30GZLgjH7GBIjXyF5uQrCkw9SEAAZTr04BTBhCfoGyqvX9iMq579ihuGPkTNBk8LQBSKLyKrKhsa9XENnQsLCKB2pI98lV3a87S+okBWTGjQytb9tbtGU8Gi6b+ingt7jxDCTxeBvoa+fFYfISXwLwWH8DA7+RsdAB5OJ/sHI6UQ0teM9I112dL+qACUhcuUINU0BB23ci09UNCnpnvIouPL9mL2Jsf29ypoH27heyqrF2qxvUeB9nNgyaiXsIuBEIglcc3O3TDlJzjjPS/W6nsmCvCKGfHhdc9xq11cGTviwsLtNDS/Onm2jINR6chUDfxxiB6PbQGHj5/+fNDlCZLiYa94KSBt9sp8NHWOL3Svkca75miR1aGFmDVjl1FXTwsI4uGeSEf4G/QyGv2UaQVuchGqk50oCKccIMNIvR9vfvsJc+hDPfEjj1BblzbO0bnjfiz33fM96KqFIlE2+W2vbBnaf+eQktSY634Am7Dh6zY1MyiRF34738i2xkVx7aU0EYGZRzuKm9/Xoi3XVrPm5p8gEQy2vBUqQno6GmwwEVtHWHji7sr6SjxwXpn6XwDY1aUn2fTGzB0pVl1ruPH6TPCjk8S2glOdFIp/YitanCi8sebPuhem/fAT2dfREBXc6f/iajil6DSvyu2wpE7i8kung7iR5/Jh8gPl5Et749E2j5IhskcTvt3muiCy91ll4YvCMYeHkSzXvXUurxHqqRxV87+w+aqe9VLmiOyl+4mun1NB9m1YZx6tTMRtRHECf/IcLs/EG9RM8zb7rteNqJeaNSdbqBEt4BA38NjbBuRLTandl1HbWG7oCt7bnkjFrBwDkb2Q2wgRdWEAduNqlo/EsGutt9wARW8YmZNLlO5ChgMNQ8UysuVtDY19Sl6UaFsV+BuPCMEDBwbosV58PceQq8l+38AjvNWcjQx9FzAf/2ByXCvnztqgjTxP5640U93X27mAsykAAAyfruLBOc2IrAwD2hawpq3cpAc6dZYSoRpMfGjSy0/AMlcNr94UU/+bQQ4WcGANIw1aKHNpHbERV/Obs+28hdiA4oHzWxC85u1yNqZxcEnyCl1Wgbrl9/2N/reaC8vV+vETWE5gEBIFJXCtttWuP5bkivW1gDXmWpbBVuwVstpTBv/gr7x6SDgX/M6pI4vWX5UpN96/9C+NhN8L48Vi4bmaDim/wGGDgk8LKxroEmRv67TAEPBQ4c0lPDtvxfxW5TjAaOocvqN6H2IdxjFjhx3XHiEH1VkFf6WSQUaWug79c6yWyMDtx4dix77H+JkKILIOGwlkAD04aB7rlNzP7i3aqmicjENRIqdA4j85oK1DThFRM9dDeP3ZetKOiPvw008AYl7dnnb1ro18tMqwHSREhLKycqqmivCi5eHy0zQ+PhpF17hNA939IMWAWXmYFxD7z/aLoshurk4ZXEF5VBMLFyrgyOnQ+i7Dq3eY83ftrx7TuVvesnYSdS5gRUPIWHg9BFS9+exhshVvWjuo1rBQPnMZewyeDIXsSBl08nqoLN5+3XTHTHMLZhxkdCgCAWoPxKtSggMJ7/jYVntAtSCxgtS8sarLu2SM4QymLExWAIcBvMcMzx3Oz/RCjbytX+3sah/KbUtphZvvh0AT32oJnUQKdbMMNEd94sfn+9N8dEjz/NzKRsVAH8/SuxcnVoZ6Ul85XUMNs3zJBo3VdFNOEdabH5Uscb2/XdkeJ0zYB8+maVC9Ed5dfrTpuV3jl1nMYAbz0eC++jZrhof5/dnJ4AsFkQYWhMlqZg4BMyVA2mBGTiTc0tJuTRsftRMQWPJD2RFt7n96dl0VIw8BaApqsNhff8a7knKK+cCl2IU319bAISBeQCeUpWoUtZD0VWLQ2/P4VsNsl3SCmfiZm6/2zW00fLPSp84SZ/B1R1HBwV6nK5wUwt9YZS71puvwRSbzHlFUTPnubQsxcAjfvPz2oaMihH1P5iCf6Nd0xuCdzO6X/LlRJ6aqyF5i5iAB/fdcfyoZM6nZlHi2ZpKSvDg5utAJa7ATgC0AaEehLirj0XZdctdIef1cksD+vL0un7yHz2Zv4pik/lOicTATgMLsj3pma40RWDWDOa4yX778LS+OHq84eeUXaJKNtnX8jYi4d2FWx/AD8lxZXwzYLTH3LnnkxIpaw4Dx/zEI+Dx2YXnKa3cIssqyLRaVX0KCQFTicqF2kU4LCmJ5830sx5hTR7gRG5pGs7I1fQ62+rkNHLy3iaIRf4VYwSFXoe7j5c7k9MdR80nvLLRht99330MHHul0aNsL9m3lC7qlaZ06VErLcZIWJ2hJF5JXAt9qla7T3urAhbG/FICc2Zb0au8vLrrus5YERLBRtv3boGWrbIQamp4vogbRfEZ+26dSy0ZqkK4WflIVodYOSvnzxKE/JOQkcShoUdBSRVY3ex2eBNwIy3YoAl6aycN2W3j9fP/2HghTe29x0S/4FXtmTmzY2cixCXt9PqUX13uED8FzcMBBbco7nH3bdHhhX0FgbEV9OcqXq6cYgHaCL+aRKKEbqlH6SQHDrcCMQwIZMblMb09ng93XM701JQzdW28v1PWrr0aoIkXBqqA+b6NNRy9+BWHy4bIq/vi4/tp00WIZSNj4Z7hyfQO6/nuucldgrrKhQ0+T0z3f+Ib7IYZtAqmj7JSOwwOGKUBfX4COT1hT0MZ8HpkwzIm20pDQX1H/Mffxvp141KGu42k8lFPAWEi+G+Awg/A2zxlq0cYeBvw+D46qsSkukGUzKdBw/2cK1x8X0OfU0+yw5Ce3v9MaDYwcGPt5Q/noiobzrNlLDu2v7XDp65akaesKIlFh3c7S4BbOoUhAnUqyUMnEn0D6BU+4D4ixA64M/A2f6goleeM9D118gMXOJywmGqpvseNdEHSzz2TV7WxXCIKaLXJgKeFwxeooVHaheirj5fbOYtUoKBe73hOerjEqi8w3m4Mcu6F6GhvoLCilXFOHzLp52MOqL5dIhp9O6sRHoMNnCBSQvMmIFcXnraRMMAeXzHzRbEhPtCZiJFEWLGHx5jA+0TyqjWhcY7trOAgbOTm1ykUUAA8GmIdLDzp3M0QHmUQT5Tl+adpntOHKA/4wym1UMrXpfMMz/IakSvZNYj5qVBFGUB5fdduW75Qn5XOfCyq9eKbYQ/lwT1+Xgw71np9SgrRCEuYr8fyXo/lYaR/V1kIbvTVypUkNkkJDN59IE8qOhkG7i0eYLK+C09JKZ8XIx8aeeCGtlBTyOjWK8rdbRjlz8KlLRvxFptBVJiGmjW+951xuq3AUBnaxxunxNs8kb4RgYuDJ5y4JAVqT/15HDEhnmjpERFU2eY3VCqFrcK3X3UIVugFr4qehrzcJ4b1lWtLkaylTx6boyJzGYvGhtfnO56qBCJZlj1W9GYY0kjEX1rv1P7QlrzsZXatS5vI2fKnoDfws0I2f3WaqEcOHPGY6kL0/Mw5Dx4Er5kZ/jlLxA9WsXR4uOXppuS/1aqrdp1Yl9TwoHtKXx0EKQBzuRSW8puuK4+fPwQHUM4WfngfSUOAiPddxck8HAYKmsBkXfvYeZd0eXH5c5M9fV3hXTFEAWkQUkJ82KWciyFT3lPDScsr7pRhRv7nVA1hruwpNABUSYDEYcu7HBAV+ByNfZ1K+XmxwL9lbT4EzPs20WwgbPKVmACfAl64C4j3XuHV9sjmG3g1PZYIY1+yBfPykVWq50eecpKa7+qTZfHcK8uT/suapBth0SuhLObDnPgf1FiRn4E+37o0b309OmjNdWpGv2OB1h4OExjS5CjvLMuuPwHJwpz2ioVlmQGdNkhZgRDEpLoemzueFZtCtGNwk17A26Ctx4/QL0P7KA9wP71L2w/42QmBnr6MQ8EpxgqynX8KeCi8S+66JzOVYECuujfbRbqO8BJO3fHP371xj80MCN41xszIL481wm3FF46Mbz6H0nNJDUu7Z6rusvloCee450R3dL4th3wSbmTw/H8L4V33qqisf9j9LDykh17oI952AIpnYFdWAPBY2Q/DUXpRar2CCw1eTq1b1dEe/8h5CHgdJ4crudvNmP1OsOX3gk0wS+L2EwZf5yHr5GMvb6wbkPqaTIjTbe0tdanZ+9Tyg83TBHtNbSsMJ8OANQkngsT4zRUOIuK8uhmoAqtAfiFFerzsgo0jRphKy8bAPVYBFjVms1mFW/0T0yw0i036EDHqhiEk7bttFL3fpDID7K9UrIrRwyQDc5YLjW9gDS1jhKvFJmp1dBNUL1J297VG64JC54znHkLZ/Qqph07QxufXr1eln+7SWM7jbpPXy4md/5iog+XVgY+iasJ9vCDd5fQW8B20GpU7iQ3b78GMJJ+3nkIdV/l9lygtZWGwRH4lWcBZ6z3T4HLfsPMyD8tyAUjP0BLrPl03Bmf5koOQ3svI5tmZjV0YzWILC71CfU17lOza4vuSIUW2PXUAmYWz8jfPLZZhafBvA/SqKMHgYNecTpEPRbbow+asOnlZCYiF1uAai66Z3ghPY7QvLIlKdGTUUr4y7HjNrpkIDCt4eUaf/dyoo1/6mnDL4yQJlwb2WP3WkCiGqu84IRmFnxb4QvDNUDTMv13oMBHobCY5iyI7kNUg/S+LzxVQA+PMLuzmnnWCPtXjBhlpc/WVG4SYH+WEXfk0+iHTTTxFQPd6UZaDMb+7ZEZa/LaFfo1UFMtKpUlAPDJp4/maei8rhX7IVjg0X3fkQM0DLbyw9CyRPcqDI5yBgAu9UNWwU7AahBTNKTcuPqvNV+5mXhyQgo7twX2IMCtaK01vkIr3GFj2KjjEaM45vRh+t+Jo/SrhTMbVbR5kTkKWY4+mGWEak5WoYtZaGXrCBJ0+cONbZN33GJF/C9vYu9N9PxuJrrofIYP9r6zBar1/lcr6c9/YsFGK55KvOKmzWSMdEHbxTgM9YC9PMQID33xzYSsZgugTd2MuHFvakVI4x856MdfKnP4Ctmnq9UQO629NjYfjqa+iRedwDu30nW3Omjxsso0OYKN/NkxeUhWxBCsgY9E347y2maEvbmLACzzBIPLJCDrHIdK8e+j2wxRLYKH5GUnXdLXQkved9DFgLStKGiKz+Q/YOI8d/92mgycDg6HjLeyAzCtu+APIKaoyLCH67lX1uqNK1fVT6y/SsyLP1tgV4oD4jFLyIFqZgUuJd0O76ZJp48jdAzp49yq87KLg2urqEtnEy2e46Ir+nMMqbQNLoa28V5ny1YTte1ipjenMBPwZeSCm0eTRjaajDSfvht4zbp8uqSPDpcnX4btRJxpEQ25TQ0beXxBX363wV/7w6GcTX08xWt6jVwLaTwL6YQ9kJG7kdls4UeMCxHtTMlFTz5ioUfu9zAEYb0VWuw0fISdPl1dHnTEQ1uPT4xYWp/K0cCZLoladDJR0/Z6undUMU2cXASc9kLq1keF3yHufEQCUAj91cVi268t9fhMzUgvpoWz7EjbbEbUT8XaNqfTRRNOHaOLj++n/SWMXR8fhcdxwFFCh+BALaI4OzbuOOo/Js7/yEqp/zt+VMmZ2D6xwVpIf5bY/3P+EvGxqKji8QaEfzn9gnCxoXCWGAjvx7sO76PdVisVg3kz+pov+2avSY7/TknW0typOvp0sY3qA0JQUQ57OSqGGLWdcMFZaMu2JLp4kAM/82jMczbq2tuE5BIc86xxSy9CcVHXLla3F7HHPu4ocUE6RTzv8zpcnhLBTATmAbRrMPI8uuxaon+3m+LCRj4FB9eefb4e1UT3QJUeSXmjJaTxy9zOrN4y7wMGqRBtt4vIumSGwCljX362gJ5/Ag5DbrMAH5NOxN5b6eZ7rMAlSPJZe77d9JwWlXedLzG8bud9kIQUsRq69pY8XCjzMH8FVFjIAKKckLKEDh8tdP9u9vw8+HPogUTIQD0yM6+MsqwJSUmyAm8jjz6craKuZ3EcP+P5ey+NzIesUK//WVhAg5FcZAzSfm4ChkfsFxe9B3OuyP2++cc93+/lMZe9xDAlAqI6fJDdlHogDCWcoBOhnJASjJJTR0yFyvwQHPPmAVBAkLirKmDfSg3166Wn24c56eorK/ZsDWU/47WtrTsQ1QA15u9/+eYWViBO1EAP3K2jW28sRkILr5mGD0hzHRVZrB4nSgXon0hvvuKgy69V0aa/fW2VCmrTygRsZiU1qO/JwBV7lCy0aKjXFVr6+TcvjbrCPjavTgMylV5cIjEqlkp3IgPTRQd3ksONj6BwA6YsX6Slvj1jw7TGTHPocD0t+hjAL+64Y975SGOKuPFlC43U+8Kc0t+Jp3B+gYmefVlFsxbY6PRpselpWSDQ0IpFBth+pX9TfO/ipaYCmhMNDbjegDBTpI51liIXlhkeRzsnIHLjVoRgjkpBVEWMaopZhOx9eC/9C5NBgOJqk9n+0c3H/hzP9fx0YvDJFAX88gCcC6KxCDcSgTUjOoTeg91kKp4rDu2iZrv+oVdOHKG5DJdaJQNn6VtLtw410XdrtLTyIwsYCCM0yerzYOZ8M1Tofa6wlmHgwjz9vcVCdz54mpLqW2nDz2z3FRyRWIr6fJmBkhI9qnKEmiwvoPc/UNNv35ZQzwt8bZ0u2rzVQn2utNPuvR5bbawp2JS0ep0BDNzfoe2O5LSIMnBhvhXUBOr0wQgv9RSrzYHEKEiM6vDP7BXM+qiJd1hzNv89K73wJDQ5PlqfQksx9bsqn778lscmTrPAgsuJk3qsN0JSlYIyDFyAXk406+GoZaLkRPaS94Ss8UhL3Hb5C/pDylzKazjaTRI1MTtVfcOFi5ad1i4rpN/Xa5FIhTHHy2sxmGfnQTh7C9nQ2PGNTaTCyo2t8pEln7bbGI8/YHFmZNaf56nlt4ra1W33kxhuZQfRDkeZq/8e2EZYTT6rMIc6HdxBnRHb/TyY9ot4NkFd7gkCq0r6Zq/z87sa6d/fDDRtop26ncO2bzl8LOCSqqQCO/Q8/ISWDhyuWlKxWEuo30A7XTYYKva/BNt393Mt1Am2RM9WdIGxL0T+5pwc+DF8YEdcua8HJ4ef2aCuJNp7ILpDoCoiVWERJDo3OpsHmISoIRzaeiPRSVQUbJqm0LxxClThkoxL1pcW+nuzIQZs4wIFWU372EMWADP5XvScCGFy0N0j2cwjzkny6DHMCxAEf97Ih61Hqhe+0L1LAv31o4l2blICgtlO2/9Q0pcrTFjL/qFt7KA1e34JpExxF4eoWAMR7ASfwWe2KaRNG0ro1ecT/FTrvt2CqZy+teTRg0cP0KWAx/4N/GAv+EIsFPa2342LiEhVuuObv1cd84zL77JyVuPzr/ptz/oP8McqVersrToG4BMjkLks0oUnaXzOCfoFKoh9HoeAMuqUiglTCmQBCjRtYqQmDZW4PQNQpKfvxhRJ0kgTIYq/f+CQiq6+yUC/QE3MjLjyIsQJpCRp6N1JarrwPAeANlx0w3AFffs9b0Th3W7naGj952rafxDhQA9r6LPPfdtV0hkt1fT5Ug1lQ7oXnA+jfw6/+CaR+gzw5rnWI5zs+fS6dGMZW3Skp/mCw7toFy7EpcFviBow0srFdtieRTniRLr7bkZrtanomZf09OZkGzD7Syg9TU9frCgBkwisEudL6QWXKOn7Hz3Oh0wJJfxk9DToCgVNeMUGE1z54CcnYv9HjtbRO+9BJexOXcxrXQ0Gr4NWKTZMElEweW66saltGQKin3ze4NbACcX/XPmPqYFPZcMptKcRaaERZZGsUlICgFWiEVgzB2PouG8bTAbwpAhsDvgXg25dIRMv/SXj3GVWNWnMxJ8AE783Cpg4T9iXYOBv5Z2gnxAaxp7zYo5tVpk3baqlR5FB/c5bbFB7yRJ3uDbqgUN6GnaXlr76TqzNmlMWGuirTx30zXo9Db4ZjMPF7hpQZsI+vHhOIg26soDykL/nyiF6+vYH/3bbnGGCUwxR2zM80lK4Rhaadlufk0hbt/NlhA94F3WCBL4qs0FUQRvzPlsEKWcUMBS8yX/UtG65nnr3iDVGpEBilGR6dzYgfVcqqOOZbC6r+tRg5rFqrZEGDi0g3wigM9uaafVHxVSvbtWXAL4A1Gmup2MnvD4PF/dW0eqP4zHiOTT7oqpWjh7T0fS5RuRWYD8H4WyoqnB0RWedgTogBns4bOdN4LAphk+EfyTCF3Lhq9GBmTj4VwAm7jqvxYXXf7/9Gxa23aWcUSaB0qaXu9qUGQmrg96C9BsN92+eiJ4AkJ8LtJthyL6UiAQtlRcF1OWAZbzOTP/8DCeiL4oRDwqVuaJih4mamsB4/079esW0eG4JDsuKEbM6d2AVOKsWPcvRCVWthVqf40IuawVd0I3ntNTXAWvvlnvssEuqYTMvpo/nFdF5/6krhTv45n9tdOV1Kvr1d3GgCZGjv4K279IDk5yzKPMFBVSAFD4qKT2qGDjTh6k/EDkTmiCfubeU0POvxqJd10XPP5lH2zc6RDFwHu+27XrEmDt9GLgC5h4OOXUGZOD8PmuFZrzN/h7+NvLIrb3Y/nJWpp3GjMylQ1uRdQ+pclNSPGdIxZZw5lkbIezNyj1JNyIyaT1U7dFQPAaqN9EvT4RUgH7lpWTW+8a3TrkdeEbd1nBZqZo/84YugFpotxsaMjqKGRLayylZNAEZ1urCnlhxUVDvi/QIF7NR65aFlJoiQyrWxOyxPTItpZBWfcwMme28/ssuN08FkIcU2Lk9ySYEu+uJkzaaNC0Xkra/t2ZBoZ0efYqlGg3UoQ5a/oGTLr848b+hZNdXQ7WpoLM6RcdGrWwtsnQ2fbaODh/hfgoSWVeDkbrpotOur8Meuzcxxc9h6CD8HY4cDRjQUhPLTNI39LoSxCQHluA8jb42SYusel6xRQNo1kcfUFPL5l5nxKo74KLkpDIIkNEkCkqiXjRUxu5ROZFAxQp43CLasBZmktEJ1Kxp5UiObnLD47k9pPHztdFzwedkuTsRIidyOez79PuFR6pk4r8cXs8Vvgw0TSzyL8rPDVStRv/OFpP+kMpfQ5pUtiuWv5O53Cq0YofsUFKjE1P6sTqZRbRwpo06d/BAqQoztHO3hV6dUEQz39HRE6MSkCLS+/dS+dunu/wbB81ZWIAsU0a3jSw12U6T37C6JSOtVkcz3lLTlf0ZElfktogEMfBNe7EWTNzreMPUSEOojDGCIWVVkYKp2UNnpi5Q9wvgLzh8dtlo9RfCPMRfEfw0/t1upHVfM7P22F4VdPP1RhpyDTu+li38m4qlQWtZsJdYc5+O0glmU2jL5kVg4vm0aIaK7rk92T1v5WYGa7aj0UjPJGZE1clwGPDeX1pEmaSc3Zqf92rZcVW487SU+LPPiq106jbCHf5ghfjikZltDv/gpxcY+Zy6jUgHRwYP0pTQI5db6rnyejWdzo0vpK/IUFzqV51wArK5JfJO7f1V6z/9VkTX3FhEwxGTv2CGgfr3AciDTzhQ+S+V0KdrrPSbW2XuRIy4lX5cVwwbI8f2e0ICo5mJK+i1N9WUm+eVBnmtPpqcLpWoNVq/Pi5YrXBR8vIfF90+wkJFRfGZspPPkzkLtIBP9TBxJSR4AxiFw+3xXtYWe+iIFqGT5WFphVh1rs3SuOcyIAsToVm8PEuCE6sFSq1PVpb3heG91cNoormZ2cgGGF1gO+s5LjywMxuTyrlhx/fzRTHxc5ue9zIqBtRF/lZkoQNRCnt3AdQl8+s2puRyNnIXrVkHVLBH4z+lZWg2SOhbyUi30/o1LupyFjNgrx18K7KUDbheCZW7nZYusAO1yUR1snieKsJbdyFG10b9r/GqOLVaG7x9AzsphX5E0lvcso3oxddZkeb1rH04NYOaQBIXe/XwyHy+PwP1pKJ3KvtdZW2NTM7wwVPn86cEDkbxKIkLFPj8S181uBLgMDpok8qHmLF5pPcVOqxJV7lQRxYvenRX4QLA65lppUHcevSodAOtm+j/O9i4U02z5qsgqPmbedkToTMY+Bw4i6YB/U3s/qqRMYN5fw0pXEyfGiU0+M+ZzbdvFe6873at4pORT8MqC394QSF7BovpQqDWQv/3bho9vY5QnaQKGPm6bxz09fqyGN6h74PcYnkKCJCYFjilFQOP3hf0wkl/bc5HchMVHT2mBEBHLqR2Vo954FbL6h/ByHPs9NTYJCqysgqeS3SuxbJUOHRYg3Anr0NlIqSDq5HoRAordHsOgCSeR8zI3dHoPu9U9e/K1m4q1P0DzEl+f/5omROJW6JLwgnP3lNCbVveF8jt3zArgfZAYj9wkBP0EGCFGdbVI22X0Idz8+n9d7VAKjTTxb111KplNLgGh4dKkWh18nvQwM73RYUUemGARnZEYhr56o8i0b+KvvkNtNkbbYhMCSyJu7Q603+x4b5tVbrr0ihtxkk6OSbQYHfaEZ6F04MR0qKxXKo302d4lhQgucl/HSyBM46V/veimb5dxbi85dVi0TiWeOtTdj070g8q6MY7OEzMc2dEpqK/rHTJIAPmxkUd2sFx5XUwe0jtY19zwH7u74zEYbdffUdIPYmcPvrYAHZgSWz823zpEJgBq/quSUymRhKk8K+ggltpyfW7srTS6ukuc+VY6wUIY3n29FFR1xwtGPVLqVkVxtRyz+9CJMhK5Hm2MYwpNta+/Q6o1KP0EAjrxhFilz9eZqR7H+E4cCFUdctWGw28QUnrlumoWRPBMZMvr/16FdCfG5QwA+mB7BYr6zWsBAxJ4xytMuU9f1wI3lfsuvEcBLlLdcaoxNw8hKxlJ4pFrQNn82bN3t5+gkPE/Uulu66lqfXAbYVbFqN6pYYbJhKjOE3LakAXA+c5GgszbisOmluQVP47AOb73WDUSnrzZSNyCMu46JGcu5OngMN9lZZ+/9N3HhTAl9bRrMlKatGU7ZEEKV1Lk5CIZsY8jhsXFn6vHkYguBVCshcjh0ZylJ5vK+ib7w3Ud0AxHCyFMTDuwvjM+nQdJHEx5ddiKw05uJssPrd33os9TQk0P70+LtQVb+uTQFnshDSODDscCETYjIQhWxu1qhQYowTfaLtvqztKxRM3fuO1CPV8l5MjxculWGDQZ19ooI2bPGeHlrb8oqYzWrA63bvmrNAEXcwXT/dl1BP7raL2bXX0/nQnwGTEe8KXPaL37NcBr94FT+zoiQYSs05rqg7PUY9LjLT+R//znffVYFyOx6fWlaThqql+83dGnzpMc3NPi/kkLzh2PClXKtXegYEvRe1TgVrnDSwaLC5QY2H4Ox9nnGz9TqhTjDiYfI83h8MF6Y6hF2MvRCYMpIpYk2mpxbRmqbM03tvTDReQsTjeW4m0kez9rMBBaAWaWyFt+VntDlW7uI8ZKnlGDIsVBs5jU9BL47Vg4F6QD469vlzEJZjX7kdF+XTzkf1+DFzsxE1BHgHer6GglgrtPJdWx+/Tn3zmcM9VfBcX8AdYF+FPRb3eQZ8gGcqV/X3t3Mi09U8RIIWVQBcLznS3easODEpFg4fp6dARzk0uxeAS3zMhjE6BNWfGnJQ3TTSDA+bD7L8RlWQQ1s9n4rzSXWeknTGusmEEGt+3VY6f0WVQYQWA26M9nKc3DskmwH/m25m3uOjocStUYYHIEJWrII465aKMNA4/c9BZHT35n3l4LoT3FMLZzYr8zIlgfMhrDRmyVQsLzXjHQdMm2BF7K0oVFTW0shSpYcrxogPyahyelEZmhERWVlhqzoE2aSxQCZ8/eYROl0rwUgbF+/RIEO9V9g3u94VQUbb0AX8pKGAzVfyp1I0GX8dKvviXwJ9BW2rv9ozXhQxldnrvbTtMPxzn7/09m+6uv81F+QUevw0xMyc4ak2dWQKIYQukzHy66U41YtV9nUHFtBPPdRRUUAjktjkMp+sfg6+G4HYtkNmyldHqp6EA0mihW5Mlotizm7b4Iigm3q/NJRyTJugyKyh8l/Ag4cRCzpipAIJpC+g938KpCd94x4nF4IlNFkFSuUoYKOBCmJgNqnEXULR8TTPw30aSioefLKSx4zj/ODM7F1TsRdSoQbAqyjB0P0CTQv5pDb3+lhbSmdf5hi+VF4AZVpbW9zA8v59FdqYOUINPPXVcrP3MrzfMTrbD9rY0DwjNIZLEee/XhWarrp/TqJOeeZnzaMdX6NSz8Azy5rN2ACK3EAwVc+YqmwDGRTbEghdUEPKbksypjcXrQJiG8xaZ6e1pPJVuF0ZkWysCxr4KYYmy5tC9n1waevwZHa1YxQT3GojYtHQHQjXvg39INF8pNyPXh92dGjdg2bzulxXw/Km4VCmCpmam78JrBwJ94gjAhMfmVOg4F+jVGv17M8S4toSKpWz56dcS2LLkcI8anYxKPlY3q4h++YqBWzxxx8I2ZBv42NfzsWFjM76fR1FSoqRtO3g0nN1esIUPgYMYh5X5lnxs7C9wS38S9rLue7fRjNPHyeFje5Y6Twow7k1uRCjxTETMN/ji8RhQEt3eQ6WFPe53744XzRaPkFPfFlA/mG44aYlQXPTx8jwyZtno3VkG+m4DX8LUSIWrpy69APu71RfFTQkzkBHpNB1kNJZBbKuQyO6VQePeNNLt93Hoke87TqSrLUBCIbVbtR4LgpOYdRRMHabSnn0amjarvD9TGi6WA+AfUplvSDDfC/U7LH68cQpOpoG3pCtTmV5livAqd9uir9+Hz59yeaABOLHUjuCQiWbbuGcMN0HF4g8AI8S5vjyeRxHN97ZAsxAPfxckDrXaTssXOQGbyuFnnjlRICzHiHSPHvW5Ww8UM4PmnrKUtmCxV7GlxNCG8XosM4o9UHvfgrzIsyE520ol5+qOlnMdhCN7UwJnnvsPPEOI3WfbeDwVJTKTjRpRAqAi7wWSNXg2ezHSmFro0sEO6nW5Ho5tSNHshtD1FDVd2i8Bmd6KSaMWB8/KEvjk9xLo2Vfg6e70mF28qnle819+UwQcdy1MgbUX64L3w9SZalyMy2QqBKn6mBKpA0yn0Vw4+6ZDBAfnQ+6cbt2nVjWWgFfmvm37rEADVQY0cl+W5ufQ8SjLMV7RwNsjdrwPbmlly9YdDjhHRCdmdTQvxnD1LbuejZbMs9Hk8QzxqaGuCDGbO80KrPTYsoF76MPH8ILF3kQuwu8V1MgNMVtx4Xc8T3XozBJJ2etOqK6rTdH/XvA38W1vwWK2F8eXeapvz0I4X5aQychHpu/MuKA+LwbmhIW2I6e9cLEU/t71HCFPQ4P6YuLBBU/4ye+Z6aHRRWS1MgMX2jmrkwHe8F7Jmz2R1m8ooKtu0MA8Ejs53auzhsu+u2OnlhZ+5J95kjVbl5uS6VkkEIrW672AKUo09tQxNxMP1E/soo0rv1++u1pM3GhO4sA0UcAvvyJwPdqLDhN9gzm5XLazEydK6OChUB1t0U6FWOifixpm2+ju2wqQKcpM36x2UXpq4JzP0TyyTX/BXux3+/Yc+JVzcbfWqJKQMbFjXVSYS/tsZRIsVLNN32+7PHyt9Jeb/oJWyxVfdnFmzm3PsNJnHyXQ0GtZCOBLile9LthkPUcyow6a4K1OlCp6zSpp2swEevDxQjhweta5EmGWCJ1ao4CviBrJPfi7Hro66cdfLHReHyUdP14RoqHY1RGL9RTwF9ABVMcHsphnBGv6Omi2EpEzPJrLYWhY9sNHRUwxU0KVDJzbCCiJf/zT4iNQqQdMiMKH06oCRm+L/nKJweRWAXpZNqvSHbC5qt1OOfHmmBP9M1J5DxUKJ3KH55FGU6l/ZSwPr8K+J8FT/cqEJKCiJdMAHEqXmJLc9vNgr5h/2K2Q2Pw/1a6Mg2d1iOjuVyCRojofiKJ3L+hegEQ9RfTaCwa6dqAOgC1lNQ5s9jHRpx86KDODE6SIcVxSIQFQIo18wloKFsMDRg6IHiZaiXZ02iIwcAv98HkJ4F591cRO+uk3C2zkBtjIK8/eFUXkC0lXWGPxHrR0gr+Ad+F1RM6Mnjjbo73shrlsGy7VIkpJ29Zt1wSqF5CJcwNnZLb5UMw2LYI6PRbs4rxBBuKQ9D8VXUh9WUyWwui+xQWa0Hj8OzsXiTsMY2v0ZkgMFTHmhnB0ewcAFe+klT5AnJqclU2N9cGZez7KO+3n1OZGiMP6L+sbEiz1kvhCHELJPth+1MR7vBa1mmJ65P5c+mBWAZL1aGncc4mwl5vxmOjcs4w07U0bJSZYRaxZrGoX432bgR6ZDxW6V9Ok16uhhSJKSmTwHHaEdFJmeiGgiEuocUN2sit1+MTv1/9YSDffhWQ6+bWBkSvos88NgFsu73dxFcykSnF25ppYKpV+Ix9gSyKLY/2WH2cEqiuKibdt12ETGsoJ1NjaIgBxwAs2WIkhUPuh+7uL2qnLOz7s3VdE8z4M7qAMXd/klmoLBW5PSCWzCOanR50BhgR6MjlTMmm+BTyrvczBFgo7u29Hnk/JJGOFqX8ldzfmXrjs4kJ69MF82r/FhsdOG76wlYY+Bh4KT8vCxSZ4oRdBhe4vVV7cS0tXDyhvnjyjhQ0qfReiN/xBZdZ9Y6GLr1JToUVXGoYZ+PuxWIMtylu2Iu7Z6h9fnQiP9C4I1Yz2ws6lE3NPiupmfX0mC88Biygm/sGX80E22hKwNVTYCCz1aC+8EOpg0lmCKFfExe1F+xDl/sUABcKtgWZm/bsdDKIME78E3rtnIctf6C7boWspBqatTBeFiAoFdJDCI84zn01249/W0Y13Av/eVd7xbdlnRfTY/zh0raxm0EVntCyi1UsIKnZWHXvs4QrKy0dP0J14ng2XS0+jnynPYxJwlrdTR3/8/CFoq3PFpe92tu545jox+0EUE+eGzqt71hPu1VpVwQKakntCzHcjWocX+dmQxBtXEDO+c7eKiotFkyWi45A/LlOgKgowtvoBcQeGTMgapYASyToSAIxT1XHqpEnTLPTia+WhVgXVehGtWqyA17qA4NahnQGM3UUJJmZwotW1NTrqcH6spY7pFP3lF/in7BUn6Bav+/GLuWJGJJpbGdMTj6PBAO7nLjoFtdAXnOQ8qosw3RVZJMe/VUSnTkuBR4zqgUronAAyIZf4oIAbDKPETgthD/ctbLseXEFsenyMOtpHgQAjoIxNnpHoRiC0WDzhkpxtS0W33MAYFqwdFGTp4mIH8rTbgGGBlKawnfsXoBY2K3CDyLRopqGXniZEc5RPwxntFJHaPxdCIcoya3b6fAK5MZwiTFNSvxfK+jzb7+WdElATA9vu/TduFR0RfWqv/eurzWjnl0CDssJov6ckulXqrE7nCX86NRNQiLyBfBRQ4UDECES0CP7d443/069GxF0KyFOyd34EJySEn/7RBo/+Cg6L1gyVGs861xDSMLRNKei9uSa6b5QFwD+++PkKeuu1RLfX+3zEieu03tA19sB+6oVCevF1hhwuH0rGeAr//krUv59/VrXQ9jt6WhvzLPQM/4HgRE+/xPSE9SN/AIlRhMbAdV2vKx8T0ybXEc3ESxv8Gj8r7QP/oQSHxpvAeI72W5F7PO6R+J5m+AX6v/GPaAXNFzutgeoJwBJ79unpnJ4mqttSQ32ustMt91jxbzXVa6mnz7+s+NAI1HK4/i5gj/Nyrfzx1ClfN1y9isZ2hfXMUKvrkJjIt/BfOiC0zMhJIUScJNE4Oul9Eta675qoah35r51Q3XS4DyoaN9FMDzxm8QmNUiF0UgsQo0S65/Y8CBN2GnJ1AX0w20BmMzveMtNmQJBien5cAWzkZkhxZbWE6LGCnYkDJdII1Vikz0Ao36gIHqURaMhhmdFeJiGBUYm4fWfXJ6f9LXY8krjVpZ0u/fiz3z97AI2nVvWBfECwiuur2G6Gp15Fy5rRkBYtKQFcYni+GflW4X6DbGALFhuADuWg3373Tx5w9JiAFHXngzrq1yuBXh9rQbgMK4IiO6OFhYCZPOZx8lHQ86+qkLTG/+DSapX0wlPsZOQiLXxcsusJDkMKt3Ylsv2vsXnHWDmi/C+o0v+GJO576LHGaYA5kdIR2nYAjKE2FAF0hp2+lAghFY67DT9raOmn5R3QbhriAs65QBVWVjRqEBrplvswY56Znn6poFQCF75h1CvpwXtNNPQ6zgIprGX+OeDSAnpuTBI993IR5RUIIDKsWh//Vj7VrZNED9ztILXK1+4deG3z5SQwo4+9FcFr+mzEh9cvk38g2kbiwBxyFkERanTu+u45S2b9LnYMkpg4GDjfDlilfnFVH2BpfB3yHvczADIz8PoS29eQ12sAyMgLjEADK/SVWMDao7jP1SVCiVNJk6Ya6JGn+IDig6wiJxgX7d1vx8FTAuhIA916o8PNGCNTcPQ4tXTjHVpij13v5FTsvLPoY+FGnpKiBhgHSy1KGv2QjjLSiwGZ6fECjtRYaoqCwDxAvvLjyJLkW/jSyqhW8V/4oqpyY9VPm60FHKqDNm9xIlGJx8xXMY75khXe4LukRDUwzw3IcR8QrDIgORd/YqQ7H2A1qufiIPifTHhZR3femuOzprkp4cL58Ihcat7UjDziTrIXC5do/r8xzxZBWtdQvTriTZY5eRr6Zr2BrsTlIJbxFvjsKi6OzfV7DILtB/mIRAi4WqhES8ov7BKcEyXrIJpS9lj0o0rdDf9xkxVgByJ6HHhM4auRBYmkDVQx/iXKO11NcsyYY6JHn+KDiQ+Gqr1Ybx1qoluHMupUJGkCRaTSTk+McgI3naUq7rPn8sH/Lvvw3xxIxGEFjKUFTwE17WCn+jATvP9BAjCuOZa0DE5oNWkaba/zbP2I0LKyJQ2X1tuQnjFeC0ubefkaev9DE93/iImSsl30yJMF7nXw3QZm3MLaEI6vitYO/15gtFddpkeyHTGY54GpaXM3U36v+aRir6ARJ13ZP59mT9G6nd5YRkcyU5r+lh4MXHy/Dh7W06ChBho41Eaff+GbUChwv6OpBpsj2G9nErDoY1PKEq0NdNw88IaRUmgvmYmnN6h7FB+o8nrK3V1YkEPbROLDSumwXDdYCiho3wE1TZlhB0vmw8rDmBXUspma+lyE7D8XKSCxsnJGDUnAAGcbMHDAngrFI6VE4ibsonPOKqLvP4f68S49elI1Ey7bUxfykecWFNFNdxUiaUQxdbrAiBzyOlr3tZKsNm+cbbx4e7FCfXZFgBIgTGQvZMGu3bLv+c6wkv74S425VNEFF5upax8dcn0XQQIvgP3YawYKvHoF6bhRAz1985meJr/Ba19czHegUd14rYXGv2SAicfjee72HoJ9HJ7nb5iwE70e6f5tuWjINVaaN02PfunA0PV043V89Iq5VAsjXrxMjYtrkTuV77U3W2k+LjgVOcgFGkO0/J2zx5UtZVP5RktfffsxHQnCxKjSsRJ+n770fUm2LknqdO7Uz/t/2Y4fe/GcWRWxjkP/nxvYjT4a6R2XfWIp5cOlJvrjb8a39xwCSkBFapCdiQDlKBxYGzdp6d3ZOhr9cBEZ9Ayi63Ek85JFLKBFKAnJ9ryWzSw04RU1WYsTaPqsQhzSvpcRgQWbVCp3j61Ye2zW4cdXCsrNK8Ghb8cjHNoXnW+AlK+miy4ogh2U4V392wzlGGqqrU8seWSpIKPg9QkshUfiEhbakXvWpKVIQ48/raXFS4vo2AmW0CrO3cApX1mO1cP5ia9snN7VVgb6UgWtXEMw8M+QGeuMFmIZpbhx8WVg5L2FYOIJ9NDjNuSGF+BV8woQQvYSUZ2sBISXwS5ewaWB99rQawuRycxY2i8x3xQc6VauBpwrPNv5Eit8z0b3PkyUlpYAfHevHV5Mi1FRx72X/S8wvNevT0yOiu5V1gk+UQ7AtCWCHTo6N2u36uedon3a3J+UzMT5pURKmJ1H+eOrohzHwo07fYwWZzaMagLXls5xfOr/XuCDjg9x3ggKanOGkdYA+Sm7nkex4kKChSKaMoHxmtk5UQWcYj289ZlKpZsHNtXHHuSkDJFRaykUJTRlfBE1aWii2fMRXrPd2w8dDunZdRtSN6CRfQzP7C1IMjA957j7Blze/iNIQ5xC8pvvlXRpXzWdi9SRt9/kKFVXxi5gBidYqMgLthmnPQUtYhfnXGBOM+YakcGK6IVxnNilcnAT4ZpG1B1+L12QLvVqc5Lbqe++44doXWGeO15XKCpc5Mz07BNF8PQOV6Y8F907HAzVmQgJnN2chMuiA3N1+315+FciTFfMWCuS/oHS5r5YiCt8yfl0tZGG3FJEFndKUy/jyyuw06XXlCDDmhnqet8Lvbi25VriKcBU57iIlUUFtArrTUSxd+ly7uIaYeKNEhuv+SvvrxfQqSrBao8A+OUQEKPqVQRvKmJEcpXQUUBg3f432XatierXq9gDd94HJnrpdSXt3ltENruvdkdBb7xlpFefS6Y7bkVYTMDQltCNQWiJmZCdHn+I+5RAo5/12DkhYUG6mpFzis7JqEfXAGvcheeB5DTaDoSkxUjHyTGa/3BKTr88vpw200krP3fgUSAMyEB3DEuAGtNB53QuijlHoAKMbWrOCR8GJWQyTYb3blOGpfT4bcaUQK6gfEQnLPpIhzVJtP9QIbJ9VeyWw8AfWga0SUyhZvB3GYIMcJx+WFeqgViLNfAFNBVetqag9m31NOx6exgZuLBy2ansnuEFZDAk0n2PFpTmDGfgjxK6+8ECOno0gcY8nOPHdKXvHgW9v8hEwx+wkt29b4ULu/AInu4smbNqfe60BDh/+kenSP+e/EZVFGC/sI2IEvFeGKukV+7bC2eIgjf3bSUoSTylQfox+ocOoaHmVXVpFzrPCVHqg4mLseLIyyGyFCgsUtOvG/U07k2iL76x4RDgFK1lJVIX5eZZ6dH/OXAYGRCKZ6O0VEkmnBAN0kX33WmlrdvNyALFB59wXK3BjXeeweh24OJjKxEH+FmAZORnN3w09hWX0OzCHNpjt9MOaxFG57syXVRQYKU3J9to+SoN3XitmUbdb6EEc2hsoyEaeMBmGHDJt7DAWYyLykRAInt4dy7qVGWj4zZuOQZxF+Xh5HTqqOHEGpEp3/1gAkSpkr7+TpBGy69JRCNAy5ChVtE9yRlUD45g52MNcPE41/K490KgeOLkYUQ7eM1JdTINtHCmAjjkoQknq5pC7KTpoNtuKkC4m4mefbkQPhnC3uEEKK/ADp9dDyFnsKErlcFogjjDFxxX/2f3YeBETRvr6PKL9fT29HwApQiXH5vdQQ+N5ixqkNgHhdZ8EJlVEp1f5ZW2UpwU7jwzo8nkv47vljyQoJj4t/98xRCsb+CZXNUXeQAMbRBbxUU//FxC+w/qqEF98WEc0T9GFxmN6lKpWpiTXzY66Y8/TdQg20FffauGerqEPlvLY/a1C5efPz5EWS037O5ienY0sms9akHcqr/aribowSFj704shi3bTO/NgfMO+sU33jmAGu2EjEadwHiUPt1vptJRMxhFewHwxIVTfQlU7uPB2HIh1Z12Z5HiBBJCKM/O3TZ67tVi+v5HAz00Qkk9zrOT2cQJLgRpJppLRb0rwBjXFohS6bmH5gAd1hbkulXvNwOmlUDLmipuwBXAa546hWQXz+IQhJbkyFFvNAXbuFmyNMB8YoR6/DrkXb8SaSjbQ9Pg8oTQ+RCB/2nDJWYunIsOucO1hPeTErX0+SdEbVrVJBNjt8NiaJKYtnw5UZRK5MKeuvlu2K7zk5CGNJdUfrHgVVFfMDMsXmrGnrQitM7jva6kbucYadYUB7VsXoD1C9yHt5DVDjHnvMcPH3XS7fc6kVo1kQZeUViJKr+mZj3wdz78hNlVdO+9sqP41lYkNuGJo0GTxt8Ew8Qle6d7OtlC3eRb/DsAljrR67CLM3pULJWdu4uRr9YbMxpLfa+0r3CaeXq0753NBVW5hc66sIgymxXTdbcUgoEz9rLnsCzvROJt2/M3Jz33ioU+XMLZlCJT1GoX4thdlJriTSG7A+rzx08cducW9vTU9yejCfJROsiYSOvrNqX19ZvRkKRUqFMZgte3Zgmt+6aQroBk1H+QCmui9uWaj4jWHQz8wyV6ymxuA1ZBIRg4h4d5LpaCTf8co4neysymTdnNkaI1ndrhkiHMqyfS2vuTV+aHiNGdUuofIaxUJV1xiZ7ateG2I1Fc8C2x0DuvmzAeDwobr1cH3Y9L8QdLYQ4SCajJ9VaugQnoNgaT8cTAK6hVMz19NM8JBs4+Lg568ek8aJaM+Dd/TzCwWazFNPjmIvri6+hPwfzrxkCodJGYx6q/uR3avyJx+cOPtGvXZkMwIwiaibds3YrV6acCfZQzKe1we2PKJZIUYNv1zUMK6eYbOFbUO+1sH3M/FXpl80ZX4TAwQh1ncj+XIYxHzXBWpYWl37tG2uHVXnOSWlk6dj3HShOB4OY7rh0w46y2VZ2Ix3O1TFIo6bWULPoWzHwYGEImbKle5iUcrN//ZKGzL9TQ2+8iGUUFGNaRnNv4+Lbghrb3gI56XGqm20ewN68vvjj+Csm7B9KoLqrbiOZkZNMlcFbjIkZEeKfgtI/5QEF9exqgxfF4aItpIRxUdmE/5tObr+ixpzyMVQEveQ21O4OhVMX0S0FzFhjo+tvYC93L5JhRD79FCydNxnnwqOad9PTjBfTUYwZI+Z4LKXaw0w6NgBWX1KAUs+EgjPg2oxi8iLV9O8oALlUysBKcnj+Nm/lOUHa7oJn4yr9Wn0aH5gWi9hHYHhcX5ItajoHakv9ePQqkJDto0qtWMGIP4InnCKz4sGB145iHE2j1UqLli2AnXmSnFXgeusffn7GwoISKIiXQYAh8SPXvZ6UunTktIw4nDMcG9fE7eSdFE4xZSGMcpC8nZ9L8Og0oXaNxA1V6i6C5GPmEhXpdbqJTOUyDiMiposcUSxUdJSqYLxD6NEBN6zfkQkL0eomz5N0IPg0fgXnPy6hP5yH6IBEXL7HlAziyHfJL/6iiRx5Qwqcj0pKdYCO//64CmvCSCTjqaqi8NfTJQhW1bxc4+oMl8OWrEul+xJsXFPp61SswPj09eE95j3a9zkHPPVEA6Fb/9fvDT0T/bmPgq9hY07wmVOjq8KR0SoVJJRoLa4Y+gglHRCm+rt8VE0TUq7CK+J1Q8Rf+xK8Ditk/QiJii6VcIk8BxkGfD8x0dnQR0h6WTyjC6r0nRmlp228KqODyEUMOL22EdvFDeJo2Lovb7KBVa3lskUJCgzo92U4j7mBVq5CqkJ/d4vL2+k0KH2HtkGt+U3YLeiYti1qBefCBIRxtHBLkQFhaIfW7qoS27xKyvkXbweeWad2mgaqewGuxZkLROD2nniYAfOc5OHpt3el1MBMOagUNRRzw3Mz6CB3Uuz3PpZYDHHL330sKOvcsNZ3TKYK3zjIDYC3ZfXfm09wpCvoB+6hju0ChX0JSl08+NQO8yApnzLKXERdt3grH1OLyWc/40/y9GwbbKCW5DNOWTlqpUxHS+rwrm+KyrYnSi8encGizwYlShGd6/tzPVwSlSmeCVkt/Mqjz1Z8t2fjxfrTTrKrZ2Yj84gywYAxiA4Z01itojMHzlXSyxgOlwj2uytt3UlKCFXGiavrtDz0gKom++8FFm/6CbWygnrIyndTzAoadhKNLhbi5ZXe64N/9xTd6euFJyK7M6CNUrrvaQVPe09KPvwlaKc5t/8zpo/QsVOVizyffq+Ydial0BWKLJ8H5bR7yAAtezcIF5rc/SqjduRq642bYZl9nTOrIjduX3Hyg3Z6UFvDKfBy0+QRhd5V5qDPG+i0Iz2O6NYD5JFxX8J9+S6BLBtrh1MXJWvxpeK4BoVKYg0uQg4Gvh8H0oQAObe+cFrACuBiNKnr4PjUlJwd056nhVVyCsEZxa4jNOQsXJ8CJDaFyPip03w6vXFNMlwwyYJ+7KC2lbOy7i87q6KDkJANU6AFlsBqmg8TPid3YEpsNRfXPoYHmqJAAxZVMWsTXBD8P1WLiyRkJVmyuTehmpUycbyE8jLmAYX0wIbXUnSLQuGru731wQPB9Vdz2qbl+hftLKniTdznLAjhTBe3YpQZ4hpI6d7QiY5ngQCTsDcH5xb8o6OBh398INbPrcY7qyEo3Wi0Orn4aMHGhf3xwf2opoHvA1Opw+s0gSh2o6p7HJaAh7OTz4PW+x50ZTCjs5fve3CJq3swME0Mg6SmIjwfxig7T8UxKptv7vqrcBb8XW2kZM/FKvsHAOdwOtxGec1IJE4yWbrjdTjl5/kwmESGpZ0AD8lZ6PXd4ajDF0+dxgJ9l/ADPOBMT1DT4KnbeDM+ogumrtHcUNG8hwsietvjEygOIGBqorDoaOnzYo4YvgVnCQqOe4EyEhLwDHhoLDruTp5vgnV4TYXXSRhcvtXfAoe2HAD45nmOkcXaDVX8c2Bn00KulTp+5ZratBTXiULNKY7Hcqk0cpnuh2uSDRS7RRAFO21lCLZraIH1bIaELSG28yafPSaYjx9jG7DtpSOmYp0Mcta//BUvfWjAxT07jYOSl0NCElYyDrnCRXi8c/NyTI3Assf4XFxzcd7i1exB3/kkW0ODMyMznQxKOt538XjEyZTEmdbW2U3CdK/tWKfmrYuDuY1zENAnHfXgKY9a/9LqBdu3xIK4JF0eGzX0TqvMVmQ2CZuDeHrtoCxLBCENl5auShg4G7IuCQwVj8dqupEUfI/f4SCsdO+49cnU6DRzWEunzJVpqlM3Ofp516KQ5CwvommEaOnAYYZXw+j9+UkevTUpCjLgVoW1efIcunRU4B2o+TDQ8qyvyrR5GPP4JmHFEFBsY+Oci6lVapdqnjiHNfAStV+0GjArb4eDGABNyiX4KbISa/eEni6hDdwW9OwvMySXYfZd9ZoTkpCCLxR/BrUkjDdXNioZxuRAyZCctQD98y6+I1axuYUaQAanw/YwGdBucabSQVIVrghMM3ErX3oILw1FPqFB1vxb/7786QUdjX/emAGb7dw/kOn8DaHv9YeIqqfbtweVGi2TUSKG4PQWoY3tm3tEf619+BSho1TozUvJa3WFhvmN65H4twkfzqG3rQvp8mRM+LL6ZGZ307fdF1LBNCU2cYqYLLlEDb74A+O1eurAPDHuyp6eJYjrxvzirOUIWJt4EaqKYhCf1TAlrqvm56osOf5z8h/UA/wbqyEaoFo6VyIskEJ0i+Xe2te3abaa+cNpi5LJjJwrpnlEWpPLUUZP2QHa6zYpY8gI/2yVLN4tmAhWqSXQA43A87BgkNPHIkLyRVsKUE6rCOdRegJr5kdRMt9OVUFxIqGKlBYs5zK7a9+JQdTVK21EgV72RZi/ge78g+TEVWyAv50yoz69guFz3b6rNxWkrgF12+Tg3tj5DD1+PyJp8gpkU1vDMXZiI3OJ2+GV4cBzg9IdL5dinEuh/j3EYmZC8p0WzImrX2vcSyyGSyIMAjPmRT+QB4ZD3r7cNvV6D7GgGGj6s4hzrZfsbOW1T9ddDMLQP5p0jiIw5+d8lqcoWSjqd0X51MN/wfSckJw7I+5l7NwYoL8I+FWvAL4HGFE9/t9tV9PKbGj9nFye0J3v2WdyP1Z1MwVs4bvfxkUY6s624A6BmaOWC163/UuTrRVEFGZCq058hiFfuAQQsDxNnhvTqm4UI9ZGl8aro6oRKd/kqHdaTd45YhX4/4FINEsLGAs8d8NbLQAZrMTUmU6xpAxVwPDUCAMZGhRbeZ9x/ZuBK+t+jJnriEQuSEQU8eisglxJmJ4RUPmOkm4awY6Y4uhQUaOBtXfMM1WpVwQcl8KxHQ41N0Pxtt3p9Z6rokzW9XtZ31e1zSJh4z1YXsk6/6jQ7OER32gEEH4Ue6tUlYry8f/yEktJTnQDV8AdO8ce+4tFy6JKabrsxAYdAHnHsaTQVtxzns86+gXPbyiKv6jYUfU2Ho9yTYDxeaZzo+IkSmjqTmXhItlW5bvK4OJ1mRQ8n+VCz9Cpif/GRz9U4XKuy9tg7PRyl0IL45ce9MKccCnctYF0HQQIPZWFhYeLpE35NCnCtsVfq1XFQRoY3770Se+/e2xPomdGAbnVL1T5MHJckj1sq79PWrfSQ1k2IR9f4PRd0M9KHs9mXhZMYiTEvAB7WZqb+V2ugcWITW81eVlev47wOsaFFcZQiB4pYaXlzVizh1N7VKsG5fpb5ZOPmTffR1m/24ddtKuuNO24Xt5OF+adJyGssl2ijQHY9G730TAn162Wk1ycxjnpFmNKwK57JWZ/4AGCVqLgbfE2O9Y5b7LQEMbRrvvBmaApGVgnU59aA+hwIBvQxAB089q9v1isBbakSLdkE+obn79x/DrXa0Rip5yoobsbMx7lIiOMOGj1tR1tV8bVwaM2+Wc9Hjjechq87j7IXvFhCSKjnP+cKeuW56AQFqXpILmoOx9MvVpjo4oEm2rbdTlPeMCKDIO+98pEj33yPnOife5ldk0ZqSOs2mJj8mS4zfyF/uZj9q4TmREuXXE1Qx1uQW0JNf2820cvPei4AEiYlzqs6sZAfPHZAzChLmidmzN6Rx2lIqldCwsRnrpx1BA3NxJJAosDKCy+5feJsBdUblfx2kBTgO7wDnup5sKsp6cdf1fTqBHioK7DRS7lEv56E7F422MCr7ywWZCcDvibEqos5nAI2VWUFZjwceuZmnqU1+QBlKYU9oENdBK/y0F1HVCFsS+xYP/scc+Pz3XqgX43JdBHEMBBLn4rrueB1XkjLFiLMEc8tQ5l5ll8Hnt+Un1Zo1xTB7Ve2gR8/oaU7HlC5GTjvK4bDffvdQurRXY8shgF9mqs39Bh7+yD4GycPElFKzjmv2+odq5aLqFp1lZAwcf4EDpiN+MErheOSKi1zIYk/lpJRehiF4/5dbZq4j+Q5C7T0+oscciVqQkLx0ShpQxhvRnoJEkSU0OV4fIs3xUSUdDfC3bgZYDATASbiy5i8KG61be1UPRnMEJzuSAdvGYx834awyOEV9SWW58NFrZAQZizSjFbufqSicRNZ21DROIMbu9Wqp8sHK+mX3/0l//Q0HbzhI2tGSwNa20XIVhhN5f28HLeBQ0Q5sXDVck4iVu0SMuMdOv4VesMq9SoLI7f9Dtt4KLxPA30r+L+76O8tggNJbS9sL/N9RPgv1iqSGeGM5cldzQN3QkoZ/bR/lvJaRZBKBsuRDzt3G+ndmQww43DvLAaUOVtfcyw8PuahKmasgPYsVLHeCsrJ1VPfAR4G7rGbK4DrrqVVHxM1ahDZiBRORdsoSBCncKwFRiTYVCxKM8GTtDVUfQgZE+cOGUm9JFDHrPB2Xl9UtQ9coDbkv8sUiBYKmMDELzH6O2UJlgf5AlhujtxOV6XQK6VOdRfAzi+X0FDgn81aKrb7mpEUCD8Lxg9AgVBTHV19o9advc9rmgIDb2ukz5eqqXXLmszBXhF9hHUUAUf5SieLM3b+YBHFxEtGXDvkkdDMeojdaNMofRU6FpBDnwYjL44SNbUKa+EqqPTkIlMgGAqUj2h20YrPHLRlGxCywuSlHkw/I/8O4EIX+csMwjUnODVvcOOJ74vV8lUqhKF5QVzMZg1w06VK5nzRUtPdI7X05XceRi2s8kbZRlowgygzQxSjCm6KYvAtj0/MR4AxZphxEc6lltSsBr+HaqghlcQvOL/HXtz7dlXVOd6y0xEvvscRPOB7qAbP7fAEtISXsVzihwI1yRb4W12BMJbODm7usCwXbQOC28lTHvYe34xDyqr5a7O/DfU6RKkoa3KypHQ2puoqqdihoxWrGdRFkMQ54PC6gRqAvyCRkQQnT3ZtXbXWSN//zCZPIY8Cp/dt3zaBvl3toLZneNqTJ867RITUPX8hPtzNxKteO64U0ix54a3XQkbAkDLxBes/3IcG2TZeeWHPPTybgGld+5zGYupkiNnO7tippcNHxMS+hmaIrZC6NAHgGzK7lkbPnnpTjdLs900h8+OVNtAw12bGW1KioZ9+9YDBlPIHyWxCAYhWM11xLaBdfST6Jo108Ix3UsPs6BC8wkzOoJr/ylpAy/Jzxbxb3KB+9noxFcXWCSkT54+2pCbT8YMDdCssvK74tvIxvNSFG6NcZAqElgJffquiP//xydDEGCih/YTcWgxQwF9d76KFHwkOdfFXYLhROhD2qS89UXnBK+iBe6SMVEEfLUtEfnIbzmdPUhq2gZsQo07AY4+0DTyaZ05SzI6tb89ei6TMTKC6IWfiilTtKXw0J9CH/7bZ6O8oUakH6qv899imQGeEoZwPlXdNsvL/8m7ENulC1nvASVNN5j9ih6frE9nXJZoP/9CQl9XlWo2VVsNjPC0FWdrwfxq1gurXExsCpqCv16vozgdt8Ej3StsNsg20/AMHNWkY+ZSlM+ZFrxaFsRsWFHJu94DzyTUOjn9/Rkih50LOxP8+tfUQOros0HBOISj+lMNjcwlUu+b/vnOPgzibl1xinwLpCEUJNp+42NGXZRVPPi/2zdpRb8FiPS3/zAs4UhOstZnKN5uXQOfA52zszkfzJhb65Wskk2mmp8lvsFNbYPU3h/59/mUy9UIK39M5HnU828DNuBQ44czm+V1k6fLvtrIXkppYQeLHvMMdNh1wdRX36XD2BPGtiqsZciZe+tlt+BnwGvh63glReY3FDSW0tXbtLqafN5b3PQ7tV+TWQk8BJf38WzBhNdXrySPAUZeLeAp0N5roPMSIBzz2xDcZsObJ007auas8Yw/4YsxUcFGTRjZatcRFLZszZauOKefgpOWfmWjA9YhwLnWI46G2b6unNUtd1KZVZOPAA5G9s65KXLFAr4fs7x8gL8NeaJZFrOXcLt27rQvZh0sbCgsTP79Rd3ZuC2jlt5bAky8KLlSXIY9xktqdPsJbMCNR0LVQz3fct8eSxUef+N+KM2og+kAfpoQh8TphasTXh/uqZUR2NAYE8ZQDB2xw/gr3VyM9Yy5q2qiILuhWEba67/GmpCUrEmjEKBsSm3j2Cyc2UtKN12kpK5MZuAi2FMHhXurGZ4j8KX3IUez28wpQ2NP2wEtT3qoyeitQIxX9PSxMvG7T+ifxsT1VdYhj6Q44bLTWGvmYw8ZqDenKpUEMOCnB0Ft+p4YpwFmyRiQm1/BX5c+JoUB4j18FdUXUQGdI+2Xu5mK6FuN1AkvhK1eb6eZ7bHTwsBckVKNW0ch7E+iR+9mJzR9uOdoI4taRRsERzULoNIRMi+hKSe8OnWaFg45hYeKLv1p8CPfdt9HhKrNQ5MD7529rcMD8oSRGxRMQ3iMmlP2X26qcAu7jLKR5qmVqxwYFWMtXdg/L5jFWoX/1nYmuGWahggJfaVtN991pQr4IxIEjeU90hf+CTUXpcfwTYsPt4jw2He3ad/4tHHsnLEycO5pNdbfgR5XobXzAzi7IQdYUEfeYcIz+vzYr/v6WrewRGaWrJ6z0iM3GGSFt8ntGKiiNceWZywYIiyECqu7TOS46crTG8nNF+YQp6N9tqv8gV2uis54d3QFRCcIOZjz7EnptEsNUaPDveFerV0zlJSvMNHCog2x2D5IboswVKnp8JPKO/4+BXKQivIV3NnlPvzbJTPv3Izvgf+Az4f2mlNY/YP4ljonvq1+/zh9S2hZbN2xMvFPHs/5BJ44E6sgp2BMsEWfiFTPqmfMZHDZsJApEGvnvQVDgxMkShDKVHuGY1t4GI2WFOUlCRVfAf7fZaAPyLsuFLatKmvl+TdtYBVnygYRUUuES54kZP3acmRTv6dp5OZ/9PlFeHqvKBa2EUqmih+4x08vP2MhoCOiLHJHlfOy4k+zF/pcLnlNNBC7nvgRgNbNdnPzpyCDDz4+98mJYbMdh41Cf/PFpQQolLAg06yWwjbtTOUa0uGggUkoyQIJ/ETdDEe26/PH/KGC3a+irssn9auisbgm/ivqQ+uX1U8mCLLOVLgJaGyONhb2U+URBgQPwpKwhqZ17e9okB7KQceY4IAwq1HTLDQk0HrxFkMCjr1S2QtpDw9LXjf0QubIdPl3LCwL6b3MHi3te0A3Xp/CUsDFx7m49fb3P8KPKwHbeSpvtNirwCXEIz1Arb5Xv6Zea/DNR1XQf5O9VnwLFxSr69gdvWIwOasLu+pqZ12ZqLdVBfmP/UgNMqvpki0gL3WsoPEiDvd0B2hhPKSgsodXraicDZxrUybLSz1/aqc9FJnrtBRNNmwgGroguFbq0BRm5ufwVXv0BkdKFwRQ0bd1urbRxia8dViaeUj+dryknAnXnR3ion3ZG1huSPR19j1yeHBdsHYePsHQlH8aB5jAa/r57r/9yZjzzK+RUl1EwNeX3T03tKD32bk8DMNp9tGwnTipgEw7r0RcFNK+4C250N62VZk620r3D80mtYkCYyDHCqgmloFOntbT4k0pcj92/rqmVVL6nayxAFw9MOmfrlPpvvfLupMA1g1w1YV3J63d+z4nPvxbTtxxxzgFimgpBHaa3E2n9bPTuLE7Nx04wkVssIRhQrWji0f9hrmCe4QObQ8sGmZMjNm5eQQsWyzZx3jcr1+goNz9y0l5/xBP7xvEv/sROBw/GM+hL4GWfXc9GBn1kBafAvSSyFStp3wFvGJznnSTE/4eNKwboGHOCf6FK/8fOLtkBZfHi5m3OCJsUzl0NKxPnDzSkzHn4UXUcGQ7ex04djiibzAQwRMNyoCCB4i3FLEO5TvgpoKB9B/W0/4AXxpc3WjudvgY3uoJ6lZH6//jTa2eM1IETftoH/sK/uMpbrV5atMC8pKhq7oJzBva1+j9JXLig/yA7HQaeuCioUVEaVb6gj0+r6w4hjMy+ctEJhEcfRibOwBgvZFnx/Rc/hpOUYWfidetn78EAAoaa5SJDwkHgqUdK3m2o0lBrrZxXPJyLLVxts4PUv9vUtHkr3xUFRp6AS1n9GmQUfJgMMSb6DNHpDnX78x9hTVksKtrBO6EWFNaG/PSrzu245nKp6K/N3l3NWpJOsIfXqcG54ZO+lcY3D0IJLV0RnY5ctWB5SBrin/+wxiQyrLqyjvK6HnP6qJhuObPUhi8kDTiIymFn4j8d3Mg46j9V1Tfe9HuAPbvBBg98zFckpqwyGIhZ77twANec1BDEHMqvYFPl5/sv5fpwNOvud3CHn0wM3GvG5UEoTjp6zEqTZ6ipxKmmY8eRaGKdl3GwZGgGQlZ8FOHS5Ckl8G8Z/xZfppR0KkdP73/gTcTB+yzJp25NjJ+/OaiM46rVpkDYUrzQvyaoGIlvKGjeIsT3u/zV/kao0iM5c4Vwwj4OSVyEwOm6qMsFn4abcmFn4qUD4JjxgFffL4sgsEcAS8+jNO+Ljc6Sgq8TzP5DDhzCNUWmcE93/Lb/wjiO2vRe/9wbTMQuCyVFUsGcbk1MwWe9H353ppVGPGKkg4cY/tPbv6YIR7vbjLqRuLGGctDMqjGGB5LSfFoV7IRvTzNRt94u4Ep7tz4z8GeTM2t6atw+Et5ZcdGqtUX06++sJanhRRJi2sdzc+4QxDL7g+fx5sRUSkN8e6TK9PxTVAAmLmLr2swZKT+Hu581wp2u6XrNVAyE8dSrLBusQAwSQZlA7QT7927IO61Q+m52bimCHQp2ILXsvc3/6ujYCS+j4GN5TFpmzcQh+9Cav/toahZpeA2V2mBduLtOm5lPPS5FvmHi8Den+2/nG81hnyVBu1Qj0dh0plZPCf8lEXLR0uUWevDxfNq+i/EtMGbuC8b9OOhTI4dOGerelJBCPZDoyHtBd9KylRwSGInehH3q4+IDm/520fwPhfXjKVFxGjtF76r8Gcs+YOTSsJYaWcFJmWbeLQcCjYSx1Jda4bYfsVL+wGNVzpPPy2FmEZsSER/euEkJiFOvB2sGgFdSECMeiaIGWtxjaVmUCInTV/LzVQmyNDqIwYXCWPjbu53F9EbBadoLX5Nwl7NhumjLEKelg4b8jeuDVzvCEtS5JhP1h/NfJA5iPnYbQPvhOydzF3oQGWVpPNzrI6j2kV1EWEPewobNm9zarsgUK0y/CwpzAvukA+Clrsa8tCZ6WSNMfMby2duSSTMDA6oypqEYBDoKRh6pkg54zosqiCveuj1yfYoULWLlu05s9OMnwLB9OAOnKOwIj+RIMAum2wioyV9Mr0v14IXtVuPixPH4XCQDEGZcRj3qHPb0qC6aAzSp8SeP0ZCj+9whMeEsTgxyclod6p+Q7B4zF4/0nQgJ/XJkkpuSVo8yIqgGvRUXJ981UVLipNzcyFz2wjkXsd82M28ljZtYXlsFJVeNOqyWpeUp+HscADiZmHLjTTe9K6ZedevUCBPnTqpJuxk/AqC3uWgDgF/yIxQzbsTh0wBSnH9x0d59Dtqzr8ZIVd05rVXvWywuGvUko+8LXukAk6QuPghdkSAGM4qrcRn8P3tXASBV1YXP9Oxs090hrSJit9gd2Ind3f1bKLZYCKKiIiKgYCsYoICEUtLdsbC9k//3vTdvZ2Z34s3u7O7Msuf/x1123rvv3nPvu+ee+s7PLdrLDTlN5Pj0bEWwHZmeIe80aS2n2qmN1pwuwZbXQ/v+pQgmfByM12LTuXjrBiFMZM09VRSM+ldyW8h1GDMD91og2+NG/D4ch5Z38PeaxrCPPtdqOlIwsvKOXS4Z8eHenS9eF+9H7GeqR96Zf1fW+Q4EcE9d7sTD82N6hZXhoZezu3TuuiD2WKt/Ra2FXR8z4JjfPp/99Rp0uVekbrNuxQ/QHvLw4mcZ6ybdqx98e3ZEPxYj5U0lnyxbWSZLV4h0aFd9hje0kGgO8IUP8ofjnxXztRP9RD3tUUhnQet8KKcpTq4+2QMtNQslUWujotpiV5lcsm29bHEGosK3Iqf14m0b5NOmbaRzDVoB0vHuPIwxX4vgIyskZq6/DGzUmsR6GFrta3zSDRkLJyMNcHII3nXd96zaQ6uHDXz4aTpAXirXCzkGVjYGUtaFlW2r1y2r8G7pIHentm2XX/fQnbViwq21Qw0EuA9n3u8VqRiF+OWIoj06+FQzl1yQnqX4M0PJB/i/hrKSNcPxqrdKvfuV4cRGV5cUxXkW8o9rbVHr7DqhP5tDoNeGAKdI+hzvzxYX/b0ipnSrmDJsiBD3yUakcZ4P4b4Jm1FNEueB49UEeE0+S3/bBqQlwToQ7BcHg14dztKktabL6O/uXnwl1+2GjQbxuAMHLFqyeiPm4jwcwupCgHNNL8Wh+LfiqJAn2qx5Tzn+hNdrawprdb/r5Og4HgOLyYUN2IDq8nwcrsTdsy9ZFWNtQ0pKbS3N2M/hi7Vhc2ClMPL4GkQhAyk79s319AqG3IzYDZMfhLY5Fz75OwaK4Z6Dld+5+W2BRj6xuKBO36+6YL1iSsfnVlgITMwz9tvVN21hqtDeu17qYi5iPdPlsspzL/EQGjovOWYjUstqVWSFdPV7/UHX+c+NfHdOrHEm6vta5Uj/gQMYob4mVud/xiYz3xnVfR6riWp8jzSY3GaV7t+OOsQLFgWjPlXjESl9qxaixUHQz2gK+wmEctXsBllxAe/NG/I6j0uu3LpeWN6XZB7QWtwdcsTTKlPMtx6kxAvwq2d3bpF5dfZ+1e3iRxxkGKrZNao+UA3WCve+BOqb10Y/6pb/0Z6u8MdnkadftALtUENf9N8B1twLfIE6U6Lw4swu0VUO3NtErONqk8u1akcaM/XzdTCpfwhP3XMYZMQDBE1/q7Eh9ZfaxL5W2c7trynSk9JhUi8q94sL0Lec8ukXmdJznzJU/kn+wgE1sYgKi4wyay5BS1QqLDTIk89jGoPKyGrBQ5cMNqFusWq2zc32yX59+VIm0hBmkPUoYvHFV3Vps6kJLletTW7/04B4OBeASfzdmGEV74Gtyznuap4u1uM7ifOnlUqw27tIPXsXwWbEn95bSUlf8jnl1bcy5fYbicAVChhUXb5s22GVRUssakAd/vP4c2YpQilUjbR35fijzXL8MWqKJGejVUuPdO9SV0pMdUddvfu5x6xeW3keGsNNllmHa3U79jgitekgV9eu3cbvWL5Qx6WJuaRWhTi7nCnpK3ZKEXf09EhDoLbwYX6enJtWO7WgK/bjSGA7t0fwz2JP6Mlr6Cul8sCdFsnK3DuEuNNpAlgHPbo+GfaGRZatKJM//orpDVHYOWe+xlWDNM61yMADUNMZL+GTDxqlGzaojAy+EAQB0fVihF0qLCe5PQjkJQ2mtjMzg/HLE/OS1EUr1BhH5O+SK+EeIJxrLGJGx3t7dqoCA3k45hsHSFl75KL7z00eC/Twk7uI6c8N4ilyyh9FBTIFQUInI1I+GpVg4/qspECucoSmZ8XqT7J+n41Au8uBLjdqNyskqzWoNgKVEaeZaih5qkWKtHylTUZ/YpL5/3pk81afzPtXO7xGPsDyXXnuZY1jRmnXxiq9e6TL4HNM0n9fj7LftG1d/4U6V/mMmRZArYYGj/HvJyM9sDsCE+uCGEg3FUBkq1E/XAcV/7l8YY3jpQf3o9aF+KH9Dl/01T/fFUQT4gGNTfNk6WBdAi+hSfZwpDIsKUOpOb9pUgWS9MjPvzrkrFO1GryJ1CwTOICENGWQl97MkgeeKFYErU/JDqzKeH2yM88p3/yoahrf/GCWyy6wyB03GaVfb7yshqoL8YrDZFpTB6YIVqWbCeFZYht5AYLGCIE8JD0npt/2+7IiWYvANZK5a2Nxd8yt1BkvtHPz4W3E991KYcGhsQW75UQI8Wg+tedwMPgd2v1VSnGX2IeJxHIg8a0R7qUbgtsSu0joprDJC6+aIIzdsnsPD7rauo53MXoRlV2KjwHvjFoCuWf3NPnuS4DVtNYVGZ14ptVSizSnv6iEg4UqSQxqux6H2bpYf5w9nu9mQIjrIJoe/9NxXUIvqVWfOHtub5S9ET9WRRsFGTcPG8fIwt0JHazuxjBpFwKisVtIVTOIcWBAv/qWR/bkM8gt9Te06PzwyflnlsilF8B8rgxVWc5hb9G85JF+qjdp97vlw8+K5bATSuWkc23ywy/UBBO3DOsStlf3+tJxocItHCCf3LFFnoFGbohS85B8H5q3Tdy4Rjls7tNEfObK61OZPfjIDTaLEq0+DXnkQJCMSCNgcqfGugp1k79kXYN6Qqr1JxHvL0rgbrDLE89lSJOObhx4CyDAA5X0uOZjvRvRe+GVAfubZMjlIi2bV66pXU+mo3wYv/xqk1//CFUWyJ+7gIDYFlUmtV2k9seNd0VfVLp7yClnPFTb/at1TfzzqWO5GzDV7KBouzc3pE1+kPlEvG7xMJabXVeY0w+GNr4MJpRg0fXr9FJZuCRNDhkYyMGNp+1UurZTR6eMfFOkY/t0GfWxEz7oyn7tpkAgy1FS8iIL4nUIoiorB/BRuVmEMp3f/1wk02da5dnHMuWCc4qlSaPqbVSMYfgA6VVXAFylXhBY5QJ4wjt525Wo3KsycsKa1rcDRarQH79htJnFd1T7sMctct69fysxfblUvKVq9O9OzEtzfy53MM82Iw3tTUS5K/okbnTq8wcmPdt3YRwv78GhqJo99XiMMJ1b5aqbbPLX7AKwKLxFqQ1Q++xh+Ks93ov7VpWG7jH8LiPDLL26O2TyuDJp3IhxDomzWFVz6DVy+/adVnn8WZO4ghA7OUdNYDW5Aqb0xB3z4+/+yzhE73Tr2pvyWnXsErViZ/xPj31HnfDmoLYD6TOgST0qvQctwFNXwQzYuE5JywqzeHzyzDCTOJ21fv6Jxa4a+N6LIL4yeeKBPTID5vD++8GvXYEjrMP+abO28jvQycJ9/sDf32rWRp5r2lKIac7UnuCKUoWFLrnlniI5Ef6/vD3pSgSvXi2pWROXHHVYYB64ze2qBZzwGmB0pSaJ0ay6cFRB/uTOrcBAr3xw5BUv7dkhu/1C3DCglbhhNo9kxFVEQf9WSrvUxt+FuTyYuHEuBLLbRVvWCQFi4jUG1wZvqvMMD0a0vXxDRpyAwSLnnenBT31BbVyfHo9Z3hzhkJ4DRf6cXVjOI6Y4cm2zHO1g4HsPw5r/rnn494LvytQW7RQzsQZTq47LKDabTUa8ZpK/fi7AwZYoe/VbgHuRp//Cqw7E21Sum3EmLKJ1iTdAzm9wO6PjhasT54Gt4Pcn3ximK4S9Omu44r11IsQ7dO2AiuqyPtZAyMDf6siMx81sgN0uhwEqk3i9AfLCr1uASPW6CbKIxbPEf6+awdu0cskU1IU+5ohQ8/dcxA08sWu74jcifnbFDw9hJwKC9DLgic9v11Uea9JCOtNNoRzO2DZn2SNz5rlk4NEib41g+3r0JNSwRsBPj26BJUzz859YL/XBc0gtmEFlJApzLzTma7ZulK0VDimKuVbTkhmb1SE3tuDtCJN6OYtDxfRSIFJdjjS1pfqCeBK/3GqoRW24v2J9eHEoUg3q/J9JBvRXgyz10N/z0pTSsrfdx3gZmn7pvw1UaSPM7ORWHeTlxi3hksuVXAj0cO8F/zYdENP3wV2ipQTy+QaDWT4b6ZDBZ6sV76K5sfT0NxWuKSgwo/58ZStfM2DuX6Tg3evZD2pmpBuQJfVZPtAXoriz/E/2HL3fAZ/WTC+it1onQvyzX8auaCctnvS/ARF7yCU8Q3+CfcL5xyCY8zMbiQXmsNBl5JVnh/lk1WrmjdfdAkv4gGM02LyZRz4d6Zb9+4Vq5L9ijiaxjGyM++mvHoKN7VNoIHc3aiZWmIjVe9SgweWrSuSuh0th6chEDXfNmxitUUBpdlO2vvJW/sImzUI69YG0orgaJ5YCA/32XVtkIzYWjTZCqE8ohgaDMZvScThqFEgBjMoDP4vWu9w49AT4dUfeVtkGsCWtaIvWRp1sFDUwiQzSowVC25S7d+Vbrme9GGTlKptccKVH3hlFjTEQfEUNvAsO/D+16Yxc5iaAd40NGc3D2FDUpWZfVIIGDwvK6LetctpJ+f53ogYYkFRNGuBWM8vt99vBh9BgNvL06PRMRKTH5mVNDmmlfmtUab++/WvdlM6x19m72bhZEwK/8PgVlSYD+CWvDv1xZ0KL7G6vvDEuW1kME7BZ3J66XWSx+JfY773SrEmJTPrULYcfzPQ/AL1gD8qHH+v+7ZvlqxJ9ZWRboVDGHVmNZVzL9nIALB3BNZ5LS53y8FNF8tgzWTgkkbeRjwbcfK+9vASY9pwf9TpuiiwVWF+IwtR2bCcxZ/HA6FNSw67YtrHczUTPdr4bGyCuMxHYpU/T2EN3IGnNDjcE7vmuOF92Q8tnO8MgVJYA0II8NDdBXvlh7ZVnUlN8C37kwjp8D2MPKvYVLMkabNkzI+3u/jtZZS4aDK1BCgotiBTPlEFnW2TVGmrfAa09G9rii81ayyfN2sk+cC3pSQdkT6/ftUnm8vDlpywI8OHDHHLp4GIgyu0dKax0Tfw+I0M++IR84ByoBxrVF26R+4DBX5fEfnxasEePFg5EE5nzwuh3NtdFf+tMiM/btvBPDHhN9EEjhxNaQV165sigEU1aSceQSHW11ytWEwCGm6t+P25dTHJin+mT1q2c8sYLAMcIqtmdjw3yMwgBTyx13N8ZXnYgis281qil3IqXlb5y7VYaO59+sUhOvcAo8xcSTiAyfx1pXnnyIWr06jXcBibhxVsTpK0mdvy101pAP4PI6IL6yUP2FZND9XUvR6DgHwB2UTa8Ckqk5keP1kt398ZibqsG/2m3j0Ok+su7tqoBiDTLD+okvkPbisFCRD6sdTyzZhHXa5qvPvkG+e4BfzjxC6zIvojmwuR6sshTQzPklPOKIcADOgcPV0ejzsJQlJy9CPn2bQBGoofIyx9htVpYgrbK584oBx9okUsGM0xIj1VAz5OS/5p5/9rksusZ5xHqymCMwItwR9Rt1bu4HBnOg3rtP6auOF5nQtw/4H+iDZxVzTzYVG7evlGnySvxbOQr1QYn7POC6iSrT6FJzilX3lggdz+cKStgalODsuo/MdCmd89Sef0FHmBUkAtqb1OLCmXorm26GKB62g3SHsFuNEG+BxO7BeZ1NciHL7VbliwtlkFnuGX+AkcU3vqAbuWTxo0DBWrmw08/HhYcfWZSXd2t1YsWwS/9Vj7BSEjqKJw9morx9oFizLSJE+/EFZvXIu2LY2QOP65AUEJAj4ne3YqC/1/w6/7tmxRfMflvO7mbuI9oL24eHiDE1eWuzliq0lKYRccW5AWNwCAnHU/BG9kX7nJb5ZxLrAA62qOsR5rQteC1QciAGA0N/FQAUnEd6+EMr1qPw+UQxBwwk0K9xygH9nfI56O1VvS0lKqzEOg3wXHeGkGwJh6M1DlQ3EZYf/1RSvhIe0QssFoZPPsyFwfXH2Gp0kGl++7br1YBXoL7VKdSp5djH9QQim1SdyaBj/NGFE64HsJGK5ygMdGDl3HYGwVy6AlGWb9+bwl2w9YDk9/1VxbJtVdolgiVIx8it38nUp7iIb4wJ+Glfat5W+mKyNxgC/r2nU4ZdCZgeFdHfqkH9C9FPm1ofMJE9INm4lQk5Qij4Z+3zhJv3+bKMFwwl5soWPE7Nea7YVY/B+VFVf9u/OE/vI0Bc/fAz649z3JkB3Gf2lV8odGcqcjGkD5PhKVhOVO5/HzNyTbLrTfA9++vQ19xgGXIPrnlXodMmMxAuMA6agzz+QlZ2fImNHCaznUansqbfw3WKo3Xih8cVea+He8DKlswQEzKszvqAErLzPLY01kyagytIKGHlu5Ay/yoaVup652UvaI1LzjoMMqgNr8yZtSaupq1OhXiOa0b8ZgTU3VbjRJw86Gd6Dvv1gwrLXg66yS3sjIQpiJ5Zdt2+shNsmZdBpalPtNazfS09lo1AUP+uiu90qIZXzmVK/k41LwDARrv5saX5mQI8gktOshx0HICaTde2b6zSI4+zSmPPJ0jJaXhYhB8ct/tbqTmqAhXpDVAL5tYh0GR1Z0FbWvzoXKTVxmXP/zvkr5iQ2ETGixKIVxYXlQjA7DSdamEQZ3jc7b5646bHQCBgQD34pnlW2vQRBYlwWG6KnxlEhghbAPiwihnnGyXfXtXNqXTmvbdz9kIYLPLOyMD5m2yIQsC/F2kS77fqJU4ouR+R+rjSvrkYa0KpovOs0luTv3HnAiM2SALFjvkqReKkKoXesi2IZL/EhyQsuqwUpnWT66Vp+Be0mEX8fTJbfNCVdZlou6pUyE+ffmMhXg5xvr3p4hjYu7vJiW1Jl7RkCg2Bdr5EC8xgy4CwViB75YsIwqZT55+QUvDqvv+Jp4DoS3u169ULjg3VAseD7Plfzh0xUt8YXKwOX7UtJWclpkdMtvrNjjB1yK5aAgKSqAyfbDrgiblIw8tQs44BbwabMcT9EtIfavLg1+849dzvSfTKu5r9hNL3xZBaWLqnd72VceNN0MjNN5ziLiyUXs8TEdoW3lt93Y9XUy6a96FAC8u16b5TprkkXsrW4to4v1tOmpWX4YD4BQGsAWiAJoBdOQTaIgHWXVG/4fhwjvoxyaY9VXXhEj3rka5YYhmDUg6tiW4Q+S7UVauTpMLryLvQyMs+O3jjVvI1QrEcN3TX0ApDC6AFaVHro49u0+vyx7XqRDnwNtL6x/xI2qCPE1grwOUIhr0ZG0xkSkPrzZpLe2okVcCovHIf8uKUNmrQO55RNPI678gv+Act1LkhET/LFOUpkALrurImXX7AipsXZzTWNoioFDlM32/Lpk0pUiG3GKVMpjkQsknb74Ik3KQhpQHUA/ij9cn4gbH3HvDoe3EaDaV81jxJ+rd/XBx8KVGCHDD1fuJq01WyN+VXOqL+5SD8+htPpn4TevBKBaGCbIiXHy+FUVGKh4yDfLtj3b4wEulsCggwGkROhKAI68huHX/MFkqesfKqoxfI+BSSW9TbjLKaSdaYA0I+IT1tpWq1y1dbpeLhwgEeajrgGt3H6ToHQuEzPidQjXDjX/hDy/R547L/2r6z7WOlx486joX4v32328xOrQr1lRsQRrTtjh9rbHarOr3R9kd8mnzdnI7cp0r+sjZpsvtRfGQIjlsEAoX/ERfblXFWVV7WHv3KVHm8EmfcJzfN44AK2rBn2HDMlbR/Mo2M2BSG5rbXEY0byMtoAVpHGSToz4uldsfcKCwSiCYjSPu0L5Mrr40UPOdoUMMaKoMall7/KmJJymBbvs1F/NV+4oBApjEvxl2xszYVK61/LlRvOvz1XsoTvo1F1efZuE1oCwcompiEDXcpnKowedpoNnt8sM385G5OGw+8QCKxFiCjyQGmfx9ulx2rQtrKqAhsqDOHcDtfh+H9sPxzleHvkeg5Z5yoB4DUjWtcv1V3H5T8WgUPycYJHjC2V6ZOafyGqUA/xj7aWukniYD8ZD8IVIqg/EEIvSLJoUVdd3nOhfik+ZO3gQmMN0sInGZbwXQxZTSmEittcbPDohYvxe5zhdmIdjID7cYeDgRtjwyY1ahXAtf7eL/EMGqmIADPtta62iNP4h6s1tuuRYxC0Cb0g4su7Fhza6CSb1id/vA8vFa41ZiJY+VL6nJuBV/5W/TeXL3R0/jG+bXXnmxV+zAD1euxML5FgFNqismNYiChylI6vknsl6iCPIDWomvW6PAwKauiZofQf5ZF24Tz2cLxQPsdBo4LN2biFzUJzWYE1cvfbIS2u9PmH9VTDIIzSjnnGaXTh1Lg9ws8P/j3XzuJWO5AFcM7mDOaYjNuAtgT45qQj8z7XJqCIYCUAyPN6Ef8buc4mJBElzM9zNvj0PufzxN1q3Xqj8GOkZLxxBA1LYyBt7juu62G/O1QR/Ii+vEfgOequv+1rkQJwMQ5fktfsREmJ9eXCzFSQQ4wc1hKPKc/9eslXRhVHUl8sr6DWXS5+ASGXRWGoKyqDmmol4Te5m2bOGTA/YLxJQWQftZCL9SIjSNQ2HGnNKmkzSHCyNAXrnuNqf8syDYR+mTgweWynFHBUBieJq+Hik9y4AHnuxE/z1dRtOx4WvmX8O+LSKykOvPfGk/sfhzvp2Ltop55LyIK8zohOLwwypxF6uBVEq61O0HlwfOJTt/4u0fc9830gftF+JNm1L7RZqYHyqVcRUU4GddbMGBmyZev7gHX65GEOubiM1IBLHVmdi7NOJx4shD6Qqp/1r4suU22e8wo7wMy2TFIjEU4Dc0aioXphMqOHn2xWFIkw1kEERdAWV9Bh40LRFrpDptJIUQb2lutQyDiAr3xeX+DV7KAmxyyTPdKusvd2TLJERVd4QgDy1mwG+xdFHC9KdpBdKpr8jr72bK1u3MKU+2UVRnGYm0a+uWow8PtMH5eg7+6O36/EoxH94TGvnbCCrMZb1whVDIAubjk88jFFBgGXODvupSBMhlBw5Mi2HF+UYnmlzMjtTwBcSgD2ztGM0hiDiPQgx0Mw5EtDojynGje94WMedR0wwlCnDT6H/E/d8O5TsTENssF/UV1vFJzUS86BOxC5awrwr3hFx08AC77L8v/d0aGRElbZOvvqHlgxYlxlSIXINU0ofwSRS9Cp+8W4np8BNAkk49sbJWmqjn1X07BilzWuTPWelyymCjrF1frJRxDiYeIPdFPvhlCGRLJlJiTvQdrnxNJO2zF959PXhB1clQkkKIH3zQwbMx+uWxOEBD6h4shmQ8v2YjoOoT+HVua9xMqWIUuomyx17Zuq1Ubr23QM65FKloawHa4UoeE1Is3sf6nhHiF59Pk3ZgTAVINwvaumI1EfP7Ay12f9R6uYccYBFOmEIzlE1DJZ+ceWoxgDzow1Svo1Y7Ej6ugiSy4sQcrM4LFLP6CZ3FcmxHRQB5y7BZvjpTTK6AaDYi4s2ycrc4ZwHQhZIe/zd3bSLOo9rVSwFOnoyDD3odDm9aJHgWSnvefWsA2pPsXbbCLmPGcj/hHRTgBsnGIfHm7MbAaUscFeJAoQWz0aR/7RUOyc6k4TEZd7Lqjtsgm7fa5IlnrXLIoFLgzVM3C60QR1Cni7IbyQRA1bbViXRX3V7pvX8lLHY/BMHhRrnP1aZ961l6263J65JCiH/+xxeuZpL5IgYa3XmJNf8GNuNkXfyKnxw+tBEozXmoUv0sHBiEV6b/VSqd+vnkihvSZOlyDY1MC8VJXQ29d09CsdZc/7nlPZvTTE5lfWH/c1h++KEnnbJkWSjO+gN3cpMMLO88XPgxao3XN1LFD7SHw9uLOceueH49m/LF9Nu6oIMk5uTjf/3CCgIc5nfPFX00+VbfWKJgvP8PpVsZYKn5wy+5wC2HHRRcl9sgV91olGUr1UArrtpGyAP/GNaexlXIAdfHRPUd378vMQ3iA0TS135tXhW8X9GGgWptPjuqu6XJgKOM8uzLWhW2QJ+UO/DeXp/bRF7Ce2ypwb2iqpzIg+VwNQ5/Oo5X7kHHDWJ6dJ1TUghxcsFmsDHKL2Yt1vVIX9qTpBqV/zwvRyCS9e2mbWQgUiYM5ZW6gueaJ9My4K4XymEnemXIzVkopIL8Z/ro6pGZnRrwImpDCSRuBC+jnGlj5ur722Xq2S13m2TTloAg797VLeeeoUYUK0IOfXkjb7swaKU+kqd5uhjP76XwRLH7TF8npnwCJKnR6C4A5pB4+DHu31I8SkGV+klvwHztIWazQixwYpGHUT5UO/zzPXtmWI78PT+Q6kTh8lBuM9m/GnngFblJ3hO9UKmEFehOPWE6BTf3K6NM/i5d3h+dIe16muEuLJaNm7mNh1o9lPgL7IVXwk1xJwKCGQGejPQKsBACleUi9xBlm/4c+v5w9aWqY0oaIb7et2MeeLEgFj9mowbvhhSINm6E0/wonOrfA5RoE5joIi3ZHYAVHfVxIU6vdjl9cKb88Sfzy7Uo9uRc6NHnKHCG5cswAXEMiaZ0bAAPI72PfFXJI3/8VSifjEvz884nVotTHrwLfk5s4JpGvgfm/f/lpVbeuN7cb3Ld3bsZBHQL1Te+fo+Y525V1x1+Jy46ydQsXTyHtdWjaSR62mqlvY1et3wKX3igEAw0vyut0ryZ5ro0yMZNVnnjPac4nX7MbqynUwAudDIqFiaWECHvdsrPqDwXSjr0vMR2JAGtaZo3RQYKE6GewdffZsoBR6bLeVe45NrbCiG8WWO98qN4ZxfgPdyPd/ah7CaSjEmL7OMOHLg2ojSvDnL17tbjNx3X1colSSPE/aMl8Ev0OBusEp0+i1phYLSHZEGQExP8paYolIBUNHtYOEF6jVnkIx+5qrvlpHOK4TdPwwuRLqVlalGV1CisQp+iS04/JSjITAnSSvyGRWvFeWlZcqgDlo7yc45HnniuBDn6Wk65T/bpViqDzw7k9/JQ8SNM6mtTpsIZZn76et3r2ItgNSPM6hpPvL+uEQOEd9mvaxUllH83HN1BPDC710eigXp0/m7khQcSXezgyRWXqFj/JAqZL7+2y+YtgcwJmnWvR22EzESnOanhByFvQFMU6jnkoFQxpfPlUoV2mdMmewrSsTc5gCmfJmde5JYzLsyXuf/kS2kpzc8cU4Wa4PgLedsCAvxt7IE3wdWYlqQaOGdpFrJpWCFQB7kOP+LwD3VcVyuXJJUQP6Xn8ZMw6pjAL7NRdSmV6FiY199BrvPEVh2lc9hUtMBoiord8gZMUm17OqV5Z5j9XszAxyEbNiV/3XJGhh86sPZwoFlvOBihrbDIKc+8EChbmmb3yJ03uZSSkxqtgWlzPCoTpYKNQ4lB+xelBXR2VnEbdFYLpPB314Y9YkKQG2zLyvBNmXbxIgCuPhLHPAHzOrzcHMp1YJKLAAk8YP+AwN66zSJ33O9UYgc0GoIgq31RFrc2KBuFV3r3SKyLqab6/cWkdJQEdiifjn1NktvOqZjL33i3BBHnlX3ewf0gd/eDAvM6wJr+btNZelqSf//6A1ZenZT3woh31ui8tsYvSw6IHP8wjQ4TQxk34hM2v0M51TKPFuapTx17kF+YXeMMSuQD+mIhf9+yo4xEgZAv8FnhL15R2QcD7RxlTvMLnfLw/9QePPeKQYCyqRDreA97Ol06tAuYfvr29kij3PCmIEaO114woCZCEsm58G21RSDhRTCDjoH2pVXyev7VEkSnO2TfPqq76oD9S4Eolynf/qTWLeZ1L+/cJn0wF8fbE20+rd6YtXiIB3A4OasE/fdrcvG06gHQjeXEruL6brmidToXB/DOOTPxppPV3mzGM8rQa7kv0EP7AmIeAu8S64Xb5aZrKLCpIRqkoNAK8CUzrlHXBgFdLKjWdjt84XrdFlXvZfCdtcXVyDE2GzdZZPnKUB3uv+VGBInSJK5q1EXFReJy6bekacGmvWwOpbzwoVBebAzurcI6Tgyf9bfCPk7VF5XubiSWsbtiw5rof3g1r0wqIf7139+tAHTHCJybX8K4ImZ5MBHfGfd2VE1OJeh2Vj+6JTNXznNkySTUgx4DeNIVOAHGelUKC4Ov8MjVN/HUGHgJB/S3StMmKstaNDPLXTdrJkXU7G5XKo40Xb6eaoyS26gF/n32SZdJqhrPUm/lky6Die7nkmLZokSU+mDa88hzLxtlxOtmlHlkcQmklw0vkUuvdSBXnzzzKkFuzN09Gj5QcyzGV7uX8Tdgr050tBLJFt7AZjysXQWDZ+y+GZFzngrG3ylAudseZEan0H7rZbPs3y+gXf05yw4/bsCKRyF+LYRN9QBVY/Mw+IrNW1yAYnbIicdFhcWIr9FKV6vR4nfclykr1oTH0Fq7DkGnS3iwDYSHqq6v4NnW/3LQbN4VZUTvxYFoIMzn2Yl2TVSTI7Fu345gaSJO6CDvSSeeOH7Md1/ruLR2LkkqIc4hYwnNxw++aVFTNb+BNn45kH5SkahxNUd+5HUZuXIVwA7GQZg/umOzArjPF0kP5HhFH9SsOaEv6/sfaS8ngnaA4d5SLUktdyFXdp+uNSNkfT4jCsAEdD0946ju/PWGRv1IblO5FbW1NZSlsV+WyBUX2+TEY9UI2RbNXHL7jWny8zRUOPMf/v6F4J8CAJgzkkwbr8gPnZZ0XWz0tQCOfxxKII8Cnk8XKtotBd4pADVKRtqBgMXhOJSVlUekixwyEAU1jgqYrRlX8sJr3KSDa4Nb5MFMRErr2rurNvKK80d32br1icxCD98vWh9uvKZEjjrVCP8/hXXijmLKmBhtrvwwyD0IWGuDINNz8C55k9bnHX3+3kCFOa0kb4yZ3gwBPqNqq6Fm7koqnziHeELfQWvwI2rNQ75z80ph9knkDlcz/I3aKsfBIgsXQSuf07aLPIhSfGdDS1fyy2O+DFrITKSf3Kz48ciUH0rk/Y/K5P2P3fL+h4QprR3GcRz74XRe03QqNGpqAQHyyuPPhALpHH4I4G97BTZPcu3zgt1SkqTpitXhme+ELmLy48dXpx3eq71jXDH72mrHbxxvn38vK5J5OJRpQZRWi0muusSIOt2Bg+2ojw3y63Sa0f0WKazNVwCr6guL5RBvDyJcj7abmozSA5pp7ZK6J3TrUiaDjmE8iHZyi7VnRD/NKIGR+BBi+mIE6n7Sor38264bAtZy5Wy8g6kqwItxSF2GOg8VgxDDzBkSgaVOK5aFW0dJJ8TTmuRuBpZ6zJMOtdYPCvP0GUBq9w2K+2lcPFnwc9+Il+Hlxi1lGnDC30F62vEogdgRGwDcdupHyXllSA5/6nmMGl2ak22SkwfZ5J/pZnn8Aaa71KDqEdQt9vVUHFBqmmjKuwllS4MPPv8sLJFJ3wQqyGVmuKGNI3pbMfMhSgAv7q+FBfIcNDiSLnbW9ED87Wcii6GjPxCIwC2WBfrreCsbkTUxr3UIT/CP2lk1+pnM/v2LzffBnVvKkdm43vfvmwboXULP+iPSxYpa9Fb4d9V/876jkNkwAAiANTkmtt3RZJMjHMgq1j+shF75+tBiefgeHnCjrwlFQPt5o+R08w78oQcqjA0CuBI/oyC0f0WQ2ueAmH4eNSNY2S0Hrh/uS6mIb6HNCXFHfi3M15Mf7r7itHOGJnSCEtBY0pnTP/9lrKeFNPt6i2wbjPEFV7wIGS4tZ5v05fQlgE211wQnpAtwwvk51ZEp812l8p8fMIVa0Sz4z39CAAbHX4S8RmcUbHIK+8wMqzxyrx1R2szXjjesKRHjrsltUuufQQ6BJt4Tn8XMXMBLWVbmkxGjkXt/MjnKohdumNiLZP6/mfLauwVK8A41N1a5Ojs9S/ZNouhZIv+djsPPq87t4gN8qq8kZm2gmBNlwI6s4KvHvFK9gBucaQEKQRDGFeTA4aeuBFG0Lo9DyiDhfbVxtWhml1FvEQc9UPjkq2/ssn5jUAESCKkLcGC26zsJ6+RYjMvicGMk5oFsxYf33yl33+KSF1+3Il4kPF47U1/TARWt0UG2dDkmHembYOoBsL50xV6ktlY/6ZsSCHB9Q9vVsms3pHskFyXmyJ7gMfU/4IA1aDIvWrPcgN8CcAdxiesz7Qtt4QJE4fNzIXySL+ME/G+brvJH284w00Uyb1JTN8nxxzhk5b8+ueMmat86l2kKMpObSwvUIr4ut3FQuVKvTP29BMUtAihu1MwYrdyhbcC8uRaa3IfIFEjmDaq6wpNuDUvrLHEOgPkYA9U91g04+LlVf/gTTVoK6wMkE/0Jl9oUaFBaxTcePa67yibduwV84aVlZhn2hgf4AYF9Yj8U3jgS6U97C2XDGPYNgJAslso6G9fWIQ6HzGvXXf5t21X5vAs3A/ca7jlUJnSYmVOWlVSM5pXqihHy9WrZacyTLz2bFChtwQxPrrfS37OsrEZz8OuiWCuDYWALgIi0t9E2oFKdu3md/Bs2X94gGdC+v/4sUyZ/7pImjbQUm/rPpVMRWNMpyP9YVOyRd0YBy7c4oGV07VIKP2GgwhktGmOBx/9RQdQzY60zryPKrvLlVFKmJvwHQVp9yB/dwhvPVVKutqr7lXKIqI0oxTi4XIZOXbp1rWwJKjXapqUN1haud3ZedSX9NTtN/pgR2KSt0DrPg+Ul2Q4kcQy9Cpf65KjD82Xq5HSk3YXWGCCnphYWyqVb1kgBrHqc9+oeGqvQwTq7ZQkO8ZP11VTw7NO3e9Jp4WRcUgrxT3/52OsQ8/foX0w74ivwae4NdXmVfRSfnTAdXrtjkyyFAA9oINo7YJAmQIT6ZIRFTj6hQCzm2it3SJ/YiA+twBUJsozU8sbP8h/XoQIVNUeVfPLtj6Uye24QihwsErdcV4Y4gcDfKCg3hKQn1dmeUv7gs6EF2fyar7cMPC2o3cOqCRq45891Sn+s4GdukqUMbUVBG2fQ+jIgperyi82wsqhphFyPe/LNct9jrFLGNal6bfeB9eryOit/SZwCr7zyFsyMe7SAs9pZa8SKOGRggZxyAg6wsNIFi2ruK78jJ/zeXVshyOu3ZbMit9egFoc7KKshymyUjf/+2y9qZ7bie0pSCnEOoWt2F2LTphY0W3y8j/vqfPhxb921WWYX0SdeUa8yyVGHpcuo4VY57URWa1I3rtojA8oOqmAqJG6Yx0HjyahlEywBgDLL/Xvsi1teHs4M0IA23rsHtfHQYJ+R+XmIrk0st9RAoUhzEH1ujODjYQi+IrnzS8U0c1NiOxejtYA2K9IWgu9EAHgkE40s2BWaNAXBdPuNoaBGM2baZdYcVQtnsBYPd9cjAJIR6bVJDPxSl4FqmP5veRnKENf+1ss94bkn3NK3J+cy9PncT77GO/BA3taEvwe1yet4nmXAmB/HeCsrQ2FbYVBRUlLtrySdbOjQrTPwJgVhp9FpJoK8foVvbG+gX5BG82ulYgocuVGGXJYl309w46RNTaQ2hXdkzh8F32N6LQtxbs93NwIca1C3vvneIGM+14qjqF988JYRRVLoI6y5DX0aghBHw9/+IbIoKn92y0dFeVEBJg4LFpzL88RYWtOAPUFMm/RfedGUAzCPyZ7OeedNdiAWhhruVLTDwLvQHYGPpye8yEnsnedO4BgwlbTmVlrsPmhXtGxeJjN/ccuxR1ZONSWnJgF86mpgLsDOp7/R+n+l57h+B76arMNMuuh0jVGTZk9Zhd9/wadbNOYRfWsTfMR1EvxZi7P6CwTCfTCjh2rgqt/v3DMQyfxcMYQSN7FkC2DT/JO1x6zzEZQzJb1A/iwqUiLQ3cAOf/xZkeOPtkjzpqq50GYLNU8zvnkTquO1QYBcvJQHE+RW3LsHz7k7b3P57VthqiuE+yMScfbetkM442c6zNUvN2qhXNoewBkObPqDM3LkTfjqtyI7wT13k5hP6IScpZx4u6dc70N6lanYKR5HxIQP5Tr2ybIKVonf1ynbOKOW6UMOd9gJOC1ElrrLlIwJM/7YzRxqKk60OHChZ7sq8NViQQaCHzvV4zHK6+9kycIloTFIt6KONe0xie5PrAlRuEHtv5bdS+H75RO7rVjGf2STQWdlwVIRGvSqFgnKl4dRW/0JwP/WtiUtFi8T9T3X7helhUB61IXTVtauU8ef5Z9ZiXp8QtuJf8dK6OOjN3Zw6wGj/tw4+2JclRntyncRmHRhGi6pZTNZbbCCG843QBZ7aOdmKaqwcbH4x8XnZyoC3OGoPf93bYy7Os/IwDq4GFWp5sJCU+rn2ao1pfLGO+ny5MOssV15Gy/D5vUssLeHI09fzyZfiutZZnIEkJ5WYCOYV1a5eEIsMx2fsxb4+doB9PiNOLfiH0cjtbAphPp90OBysJlSiCuHt2+Wi+H6A8Rnik+n473eLYVi+wcpa4e0jh6hjqYN0zeIp1jVavsixWgg0u8K4MvlmElMyQmO6KWWPhEaHBHzmK50miL0gwjf344SlLTKsOeNq+lfZ8nICSg3Gp4MsnkrUiofYsxIoKb1iejTgagVnor5zNV5FyLdm5Xlks8/MMl1tznk+1942FHnVjH4Yx4Z7MnMn9dwsNRiM2qiH3XVJse5BXEwGspjjH7kj5ww9u+66mus5ya1EG/bpV0ehDhN6hGFODWtrZiM+YgyZCUiPRtwLKYk0/dEQbpl+0ZxKZCswQQN6UybfPhOYR34v5OJQ+H7chYi1X/Dxv05NFluSswLf/rFAikqyZabh5RKhw68LyAMGbx1FvzpkdaPeiXKeuKCF/bskIUoW8hgoIqxCcp1ftMpz5Tmbqjl08+PeRvc1T3AJP9hZfnGWf4V2p8Klwn7QUS5EzCGpX4tzj1/i5hRmczdPifqOo9k+4hVFpZ9N6/PF88/qheLqWkHp6XLU7t3yDRAA//nL9gTvn2Vc6XY+Meh3yqpV/K541CkhsTo8KtwwOpsscrFfiAg1VSvPzw1E/7vgTDx/xWmYMWLr2fJR2NhV/HRF66KbDOe+TrSppD5nDT7Q+0WXAleeOrvDHRrjyDALz6yyqnnZ8lvQLPTAgD5Pdf1ZBzMCGU7msh2SeEMqDyOqv6Fa+4VHNp1kGdgl31emrki6YDayrue1EL881/HL0cs5fvQCZ7hnhKO4VQO8iDE/1OEeGj6hI4JSupLCAT4UN42KQsCs9Bewbat0+TdV6nF1aKfNKm5FeictuHQF/kftOUFqAjGTYn/e/nNPfL5l2litxuROxyIH6AZ+BgIhki7/EaYyydAkH2MQ8E6pX5yeHFv3Rcm8fN7KT5krk1vGqpmIeWvIhlgejcd2aH8z8Y5m8W3Ok+Ewn0VBR60Z9z/HTRO7Ul0lFi/WSGeG6CNR5gLRWj9vEZczvijjHmvCf1wIpBO28g/RrDTNicN2KFP1CpWBboRzjqg/U1FyCPRMkJ8hzTAkb6Rv1OOgI/6UhyeekGo641PSMfhojcO7H/hEKVN2DujXDJuIkFdisSpjF19ngUC/OmmLSUtiQR4Mr1GLBL0+WiLnDHYJn/NCZRsZR95+CUY0nWYq6G5zZW0vPqiJK2A+0enFu7pf8jh3zYI8eqt2gW4negNUUG4uSEQ4YwveH0hWhfG7t5Z6cVp2tgmb75olOys5BHgi5ZYEDyWXK94O/i374AZ98ayUikpPwj5ZONmblZcJ2r8AH9rDSESbuXQzD7XXSr3okDNKrRD6RxNo3VCizUXuMTYBKbbYzsgm0cNaFLMlEEL04eN0dc0KOL7xM5qX+C3Nm4uEvPCbeL5C0VddoT6dV3/7RDLD6vEdXyniFHEPrQR1pQ/dQ2QPVqHFZaKL/yn1eL8boVyeNBoG/z6ikaLC4yZgABu4hAjcNm9Z3TXvaGblmIN/7tFyUH27igRDw4JxZiPNTjIrIF2/w0OKgMgzG+Hhs6CNrFInS9LyHzl7XZK3m61rxqnyfk+gAa9OMkKtzDN7M0RDkAgs8pe/IetWPyJ73ufNGtSLJPHIUXvhgyZ8j2rqwXiahSNPH+PnAOrySDwUu9BK74+1P7VEwsKQlIUI/UAcFp/Dv/wvYW130P9T0xqTZzDOLBV/1XTNynRF1GF+FoG/+gfd9JfuRQC/MZt8E2GBMPQp2iSV4fCBHYSX7bkEZrAi5BNm2Om9dcq38mdE7DxXArhMBImYVc5L0NFKv3ObzZuFVJTWhO8Y4p3y+M7tiKXVNvYovOcj3CtBHYBLOXGWRvFiEA0c/dGUPM7izvHFhJ2GK4lHwLPvJ2Rb985V0z7tRDzy3+Jp4hCWWWdF75q95eLxdIyU1x9mlYKYzS64XZZwsQOlSy9molr6Q7kqXnFu7MEYwxvUmbQm3fmBvHiumBisJgpCxn4gxBUB9Q3d++mitjRl1qrtmTokiuWk7uIsRDPwHjEr+krhyH8fzsOCt+68uS34gK5EnCo1yDXv0mMrIarUMFwBjTxH4jYpjwldE6ZTtYVhTreBdJc8pFP1qyra+EdzBWfNG7kkbdfdspJ56bJwsWhGS6cp8eQQ965eVvpBEjgVKctCISeHiaGJcy4vDnGjI1bvDVZNrb63EzaFDNtaM07tN6I31XUiSjETY644vWBuM1+Au0kgEbl3wyxse2/nw2lRbEZJ10UurJdJx37aVp/FFG2CzrsI9ehdjR9stzgTcASN+H3S7Ny5bOW7RXzbOi2pv7rcpSLvSC7kXJtcIEVU9tsMUAb5ke0z5HtFT+yVoWOYsWzere4vlspnvt/FOPbf4t5pRqNTk7F4panHZ4x7AQxX9RX6bN2sPCidqb7zZlihlCsaHgyAKTFvYJxADCNZwAyE8LXCMx0ks+JLI61u0PGyTaNe+AeeOkvca9Rv1P+hobNOEiYXz1ZfEOPF9egzuLq1VQNiotyjtHGxSea4Bow/LhKDLAceG77Tsru/kHc69SANO06jQdskoGbb+CwNWDdMnl2d3R/JaPMRzZtI49DSLNIkDKn/s+RKDjyOgoI/diqs7SqB0Kndl4qn7RpVSbz//DJkYc6MD8B/Y5WnbWwQp22aXUSqQ1V5woBs+bokxWuAwfulzyFwyMMOek18S9nfFWQKWmvFEjJBxhDxP5Sf/gJPsvjYJaLtTlWffpr584d0PomQyupuFm2b2uXn79ySlZmcmm85VyhvTR5jAOBbuG3LKyKx3KbyY0QyMG6ZlOY3ClwInXbhC8egUn+EORs34sAQwoaRefbViRWlPx0DWTQj58wYcbT1IxI84Sl4kWQmHs9BSOMpixaDX+zaRHM4V3Qh3N7iLd1ZkRjqtYmMUEMR7QTGzRw1+Rl4kGqmHI4QHuGx38VM8za7sPblffBuAvmar+QNOWmiRuC13JqN3GOXyxEfrPAtO1BYBxJEbT5iKt4cYY4Eb2uCFeazdMsYj6vl7gPaClOe2hJ12hvgHI4gYncvBYFJd6ejbQ26HCFaonHYFIPHupbqmnjyu/+Be+AZeQoCOJYxBaugeZ+Pqr9aZHzvCcbgW9KcRMlDiIZySDt2iSj/gSri7EEcM1WOeoUh8yZH8A3IR/zsfafxOHqYRyK9a+K5OG/JhdehOvVE6VwVFCPXT379f/uqz9/T55BhOlJ0gtx9jnLlruxoAx5ViI5EbmJVfYbwFC2wlTCYhipSiyLd8n2DbLCKKcFAACgKUlEQVS1HBNaHYnNhlKlQ8ySnZl0+PtK/7p29srpJ1lR/jO5nRoU2vFSJiwgZ+Fw2KRZW3kNSGHTWbYQ1b3cnywQC3zU7nP2EQ+D1yA4PNmqRu+5op8Yofma4Ns2ri0Q74x14tqNoLVSl3gXbhXDil1ihqnbeCaEMH3j8J1HEjg+WA3KTumCVB/YX776T3x+k7cbmq7p88ViRfCcqz9rY0NuTYW2hIaUcrUHt1GHmoOwLlgSfMxw+HOjmA5qIz4IatP09eL7bW25AOel1r5IsUM+urNbI11pzYrWTosAgslMU+BPR5/c/25V3EDBh2n60Y1wFRhRJtVwdnflIGXKR8DcP1vFuWircoqi9t8CWvUzSGs6JI5MEwrt7BQ6uTM19JZrifGebJgO6nJJT3fLg3fZ5NJrzFIcBDDEOR0BS8nVsF5VBU8h3veuZq73oeqdrj3K11hsXz739iu7a6YfiWs1/h0tcc/W3dLGsk3TcPFcfI6JdBPP3Osg+IqJ/VuFjVp3Z2roQs1U+hU08AU4jIQGJhmkf780uedWmiKTU7doBJ9a9641xJwkaJZcPwz+9YOA+nU1tt+fEbXrLXGK84+1YoUZ2nDXQYogD54dj9Usnv3ha+8PgXVyZ7G9Plvcy3YqkdpeCHPnnI1iBoiLFUJVcuziPnsfZVsP6yvHH8vQhhULxQWfuOaT5qFA3p0rlsPg9z6wlXiW71K4pawnaPpsy3VQKzF/tVSc2wrFgxQ1K0z6PsC4uvBsLWpcCWwb0Fo5fHisppgCXDGHw/Ji+WWt+H5ZLV4US2EQYDApdalxoeWC3uJtmSHuHo2V8Xlx2rBsBXTwuJnihp+et1GAXwxI1Bey4XPH78m5yhO3EJMXAY+HL4+cdVqhvPVKplx+PZWGgNCjIH8DqVnPAU8hFWkZslVWV1CQIoyjrFW7Nj/vXKemgSYzpYQQJwNbSO4HWyTvMPwaEXKKgu9VgG+8hnKdqbgJUAsniEVlVDazPHxPMprf9CztFFKRdAyH8JlvIG/2cUSX/4LAKlpMXBvzxTJinhiOai8upphVJCxGLzRRuam/GMtgbv4JPuKZG8VDzRwr1fvXBkXqmv9aL+YTu4qvRQb8z8D45h+DFzJ+9xzXUax2s5R98m8g2A0X8TBhmrNJPKg9rpQe7d5YXH5tWjGRd20kBghxClH3B//gAAIt2C90OUPWfi3Ec7lfgEfjA4Uy/PzGaWvFuxj1xgvRjr/MpzbTRvjyTRDackxH8TVKEycOKAr5x2Km4H5nrnh24rDKv6ODZ2TlyONwW1CA1zdKxRHxGHXCsWXStZNVlq8KrcOwBim9W6EsNa8maE/tzzMLHbnxzupyRzoXrFv5Ye33Mf4npowQ796l+4ItK/7isTAqbuQabKpbUnWBeVwyEznNoeSTSy+wyeGHqOAVyU2h/VvNSlPoc/jkreQeSbTeZUK4DsNBcWZGidwAnOnt2NTKFiEi/L/tYjsFpuKDWosXJnJNq1Z86Ph407B0kWNhOLenmI7oINZ5m8U7fZ246Y/GBTS3+z5dAJOzWcwQggYIXsGhwItIdF+WquV7EaTmQgCd1eUV14TF8Duz6IzaW7cfZc1ghF2K2q8W0Ebhf2pX+OORtoZnuBGJrpGiUTss4kXgmgcum+AZ1I6NNM0btxSIEaZv72xo7xDCLvi6/fJX+WmCoDb1x7gPhjafaxcn0tGCiW0ZnciNH79EvDC3u5A6x8NGB6T2vdastXQHVKu9lnH2a2sFrsF7UPlgXltPr+pzkHrW1In67BlyzyNwxQAsSaPfsUd9B+/mFVHAkar61Jq9zyDvAohIxy7qbWS0/rLLW7uVA6s69pRR71q0bv0vBrks1kDnwBQ9rTQ5/cax+v5DJQGuBhpdc7kFfqrk9J8FxuQTc3n1MFVovY8yscQVr680EDCerzZpJWdBi1TATxBs5vwayE7vzBHLlmJhJbJwxL96mjnEeQJywwGjaj2lm5hhwqbfmuSFL92FKHIXNHb3sD/F+MF8MY1dJJY/1osFQptlQl3HQyMf1AX3VNbzzL2biwfavEaKSR353aa+zZX1FOKrhkXBfF5PcVNrD+osrzEjMM26uVDMnyFN9u05SnAc++XxC3Ajnm1pliGWC/uIcUh/cQ3uKS5o4d4KApzNmtFn87Q14vwFOe4Q4OxHNtbLGxDg/S32eovRzbGPYcW1oCA7Mw5XqaCdUxu//qoylDSunFb2IUCAWAUslYhFaTfpKznsHnT8cSmhhSvvVqpMwthfx1OKfYrPAfhEDI7kspoBIT7YD+mYKuNbAAvCeMJVlr8Yio4kxx6RJoceVJy0QTAaf/nCP/WIW4a+akbBkeATbCpsV1VfJYfDT05fuQOmxU+AN818ckXQPfazWI9C+tmFvcL6ubXtz9UKej0izA2n7yPmJcA2h8/cB/O6Nw8mZzi+afJ2LkDgFyGPKIA/mq8IbstpPcQHjd1yVEdFMGrtKdbojrniDYOvbujeRAy/w4ftH64ihG8cIO4+zRGprv7VPBXfw89uxIGkDAcSZTn6b1D94Hj5cOAwHocDSPN08cCfzxKukbZzHkvMML+7X/pTCQYkKf5vHHyug/+7kylltqCqL5LyO3FQA6/eGGoDwArjW5KdfJLuKJP338iSy67X3C+qMrELAcRL8J53N8cG50mWUQ6DL38FUst0HD2KO3bu9j2qBCRL16P2I6XeoBbSeO4W2QlJJ42jjWoaMJURWhgC3pHsszEH4ANrkIsZog3hjT/xeGyYhlSxLIRaC7zw8Q9DNOvQRmGww5N9QuLoH4Xbk0i7uSGzkZy3eY1swIGMGSzOaavFBMAX0y0DxNUpN+LmochJBIm5ejYRIz8ndhELNFffiL+RogVwFxwKlHWB/yh52hDuzolLlD8YGISms6/exTgkKCcBNXLcelBb8SGFzPTILwqgDMkFk7zmKw9WtHi9pSv89KyiBsuB26FuHdHsQyydankPvm+ktWkCnDEFtzVqJrdlNU4dDUInfytexoPtHIA2jYbWGjpHqWWdat7MA0ugWQqxFjXaAb/yAgBspYoQpxZOf7iOd4WXbHl2+CspAzqSUkL8kIMOWTrhr69Xg8tRhDjALnDBbuyiuSniY+Oq+RzFBipuiDk5FjnzFNX3mPxEaE6nXHGxQUb4DVEUAtvg52emsC0lDIhV5zL9/u2hVY5p0Vau275Z1mPzLsEadMP0bADIi3GfpmKEX9rTLF15SJCCW/5Q/k2J3oZg5e+G2w8SQwm01+VAgKPQRRUzH4SstwAlRSF0+TfmfsdLmnAuQ9qb8EMKMpjwVz7fjGh7Y6ZdvIe2EQ+jywn2AvO71v/KQivQjOlvBNnBHeBEJDzbJhBLT+TaPwDAnaNQVGVvoa3IrS4Nyklu1cImJxynYtOnCh1/dIl06eiQ+QtUIc5DHtfpJ7AcngeLpw7BWOdDLUSfJxbrsn64suBAAsJDnfdZbwdSSoh/+dfX25pIxrM7pJBm9QgBbgaAErjlk6I9chPQtlKCsMEtx6Zfkewwl3bqmCpCnHu1V3p2p6dDEwMiP6Ai18ocp/TUgYmdEnMVo5NdYV6c1qK9/AjLykuodjaflc7ysGn/uR6QghvFcmhb8UKYuwHEEo6CN0RF0CMHXODLJjlRDY14OiaYpy0bCxBtjmIf30GwV3EXDb6NXlrNX26Cps2ocl/bLHG1zy4X2noeY8KhwzgOvnNEy2tpcBTgjzVuISch1771XoSgxrkaDmCR4AlKRxBh+7bE7k8tOvcMM4R44KTHtbAUmrhy3FOAdVJgPPr66D3v9LO+fv+rcSkwILWLKSXE2WGTWNbgR+QodQaQYFEtdDJ9J4rzPImmaJELEcOVdmKTfPAWt9bUORGSpddfbZKhr9lly1Y//jLGRZP6KASAsazq3kAc53H2dOkO4JKX4IebiJzyMmhjXqCZOX9bJ8a/N4sVEeY+arfI7fYxijxog9F+Dcct5hd7OyKFixHt0OqNLbLEszmArKWHv4pfG35wydTyBlRgGCLIkVwQNASYIcXa95Sr2B4C4Ey/rxMPAGScjH5X9naDHOZIl/MycpQCGnvH7Adm4Acc5Ij5ECAcZh7QM0PJdQ3XwIH9K+9DLrjL6C7YH4GJyU6v4ECtx2YFwNlZEODEJEkZSjkhPnC/gxd8Ne8b2gDDqtmK9gLB8Q3qF7sASEDYzGSnHwoLlE0+mFo0M0jbNqmR4hDc7zS7W157Pk3Ov4Iaufri/450lGGFeUqVqrquo1xba4HLjqhWw7AGb4EJeThKmP4Gq8QGaC8eFhuBBk1hav52pRiRnuU5oSMd44qg83RAXXOYss30YSvqrCr+jBtQ7IM55Vgqrq0Q3PiqKlo4WzMhyE0QVOdrjFS4FunijlOZYhtGmPWNa/cohV48CMpzAq1NRYvD+QJVxk7KyJYHkfudkSJurUSuDZa6HArBEXw437+fTU49IbVM6RpPmjT2SZPGZtmxMyAKCUH8Bdb1/ki3TGYqxmFjBQFeYr8sru7tO8+et3ZFMg+nUt9STohDgNMxw1SzftE4zaX2CQQHqx0lM3GLDvdaH3KQW3p0oxBMgVNICIN9csShOJ3va5O581WQCPqG34E2fh2EeFDxzWSeloT1jR5kRmC/mNNMZqNU7khsej9BmBfz0IapdW+BMMbHgBxzEmfbRLM54FvdMEnTJq2KdtVfrq4GNTBNgVbFL5lI1XJig+Kmqod4LnCOW6Rq0KhMZkChEyurp53URfXVQwv3Ime8IhkA92pEipvybOSc+2agyh5Lpgb1yYG+nJyeJechh5iR+4Ee6+lZ/biG8/QBQJsWlSMvqrN1181mycxMPVM6Z2XfPk680xb54efQOfKlwAFtE+JypuGd07GTOo878qjP533YIMRr/E3sZGg/cpVv7el4UMT8BsKw/lZcnPRCvACnRAq4ShumGrZU47xM/ANUkIgbABJx7W0AKPG5kCPrlXxEhl6+ZZ18iHKGQPJO/GOTtEV141DHewDyyg9onCbrc9wyATEbM8uK5A/4zFkbRdtgFEjW+VvKR8N0rFDftWqmPhDm+sMRIJaDA8JlEJjjUfzn9q0b1GvDsFcVI0Hkd224od0LP/ye1gH8NDZJFwuhYCvS+j3iQr10jTTFhn00YTO/FiVEz0Exkn38aUfBY0/S6Ul4tzhb4wCdPHo3UgXLNT+jHH5wmpxxSrJWH6waGzi//5SWKFgQuUmK3kashomwBOoQ4GTC7hc+HDGratyou7tSThNXWOUw5cMrzp2naSTW8f2ZWpwvs0sbyQB71FLkdcd9/5MrLzAjcMgZt5eapjcGuF11aZEUF2fJfY8VS2mZGpw3Ay/T+VvXyegmbaQxNDadL1adz0+iO9AWgvdWpFi5pBE+Ik+gMtQWpOxQgE4Hj4r8rhX++9D0dAEWWnkX7m/UBFHwViH8hiXCYcgAHHMjzn8eP5QT3dtmBMK5mH+uCBaDHIADAJHmiHCo2uUDEfNegrFMXhp22CFzBuGdhXk8GAeKlwFFi8Kpe9HxrDJ7KDA+xWHqvu2IzA/Ce+i1T5r8OMkrNqsuuM9EL7fEtRcG8P3fshLZg5zx5BTiqsVqEqwiobUowrLEM6D9Pq/PXguwphSjlBTiffr0m7nqr1WLwesjo/GbGk5KhIVxpZXvjorHUq6+JGXA9MJOgdHgkVuuz5ePP8+Q2XNVQcF9bQ40z1t3bZE3mrSQHFSf2puJQpjC+HmY2kmc+b8R5FiMADiNDsQBNN70PPfMDWK8uI8Co6qRkl/ub3cggs1Go972LmhQ63F42Oh1yag9u8uvXYU+BKdFBc9RBlDl2iGQiRrnvSjtmgshvj8yD/bWA1k5fzF5o6E0PLZjizjL41sMkpFukfvvhMnQSjN6anJJsQUZ3PLY/Q75cSqL4wSV6VEsOsm6V6FQEYILN+vDSnd36NHlrwYhXks78qS/JtANB0QdOQSfypiA/n7w9DWxeDc0heTWxGuJbbX+GFZD+vyDMjn6VJusWedPR0EvpiFa+0pgMY9BaU9Eg9Z6v5L1gdziD2CkrzlgiFY90LHpQJTubAkc8k06KjQ1hukzG+bvbOR8d0TwnQEOjovSssoPEj9Du9odhJUd/PQWOHgdgkpuJE0xS03RFJun8VwxBQBTjwAfwBUUoGpA8s8LT6XJJefTaJjKXFL73q83LQkU2Knj5tsCK0GJvliRwnHfTf41njlPlmuT9QgVkz8n9T5+Mi4qiHYhl96/JfRDJS8pfYsdNZm8A4jRsw7tSmXSp0bp05MAH/4ALYx3ZlGhXL51veTjVF//C0/qnz4lsIx+cHziSckj0ExWFL9kMI81o7f2LD5H+7CK2FEISDszLTPs5yB8p11LY2Vo1XD946wvV5IDHxblyc3bNigaeEBUm+X5J9NR94DZsKkswCvOVOhYqCj97UzeYL2hu1CYKDZRKfSjHsW+ONmuSFkh7sjJAnqGrI7F0P9QP/ZH4OUmqyB/CP7Q1DnXxuJ2+O/79CqT7yeI9NqHcYiBmZgB7eWGHZtlg76TctUevrfcRYtnlLEaP1pULkq621IH7zrZp28krEqP79gWZEIXsdstMmq4Q26/EbnzJn0ZA8k+zkD/QlcZhfgU8CAZiccNgAjr6ZrnspPOeEjPhcl4TcoK8fF/jN8Nhk7EJ6oM5Ol4K0wquqayDmZop76qOnXQs8Q9kmb1ls2L5JP3zdK6JTVy1VfLOZmGoJN74CPXVZYgcV2q1y2Rr0bCtQaRt6BUTQ2Dpn0uUsCS9X1IlYnhpsOMgBd2bUX8gCaoEeNgMSOVLEMuv6gI1b9SMUU08gxYEZh3FlxjlTB6k3TSfoLyVhQUXxKlmwUtO3VKuah0bTwpK8Q5gH2b9v0dP6Ka1Hndw4gWLUlWVTxJX4DEd8snfXoVy4wfvdKjeyCMgcKEIChXbAPS116C6JZ43qot+iuZqu6ZD/8pf8zeArBTU3wN1+6E0kK5A7Xk9yB1UiXm7Fvkxf/Z5amHkfevCx+sNntc/WdZzB7p16f67dRWC0sAuENUuRjkQ3T3T8+/+TLwcVOTUjI6XWN1105dl8/f/u8a/LtfNPYzrYbY5H1TqGxeai6n6L2m/7Btm1L5brxDjjjJIWvXM4UOfkTMzwxErZ+3ZY08gIjngxGkVd98rdU/Q/pkC9wO/wBOOBIdBzCZhUoMSGiUAeFQXdvVXFl+8wc0lGU683pz4Ws/EPCx6s2RRqG2HInqi9bPEW4EcMiPEOAPb9+ipOtpIYgGBAoOfyldrrsCcLj11M4Rdh6VP1Z/dSd6v1sFAf4iMgUCqX4Rn+Dq07bzN/PWr0x0F2qtvZQW4uNmjt8Ew+zPMGb1BMciRqkrpi+Ybfv6U3lqjbs6HtQB6Tm/xjYm6GgpFS5RQ6HatimWHyba5ZxLHLJwSZGy5VGQz4Ygv6xsPYplNJcjEUDVJsWKZYRkCvqnQ9ve/sOmUhIlgPFrWCPmxQgQ2oXCPstRrjaatNQ2Ws+qPLGuATgLIFy9v6wuj51kF+7bvlH3YsmCEO9hi46NfQ7AZnpR0Ichjr9fCmBrx2JIGRhHze7uHZtkSSnr8mmcVtPI7rk1Ta69HBq4ISj9KlajDd/XGAc2uD1604vdBx9xxFfzxjQI8RqbjFgNZ0nahDwpGRJNiPN102Kgk+3MeD9Qrj7as1PPiTEWK1Lme4LBdOtcIl99ZpMjTwaC2Uamn6mbXyEEFcEyOkIoXJqVK1ejRrepBqP3K+qQwdpGxbWiFB+JoHX8g9zq9zCP4a13QA8sBTpRlAA+5bkxVdaA6Ig22cp6R6lSI6BVzShy4t4c6nGKh500F890axHW4d+eWTh8RSLecXImYGAqWDX5d7vJIEObtBaCpFQkI20xMfmh3hXdDlC914JzvgRxK8/A9z0NSGzEsi/Xvtk0Uu6eftQut1yHqnL1PkQ1PC//QS42seK7JImlk4oC4Y31ZP1kieWn4WNG7a7eKqnbu1NaEyfr+nXdf+O05dMJPK0mulYgTcv7ENCm10MotFbyYnXsl7U0Lzr3qVrqTW0+xicd25fJlHGZcvEQoyxcTO1GRbSimXIlNM7/wRw2HPCVt+Y0lg5mqxyHetTKpo0JrO5hLKBHhY7ZiC++x6a0DlkNFWkVcrDHcnNQOhH6LUObKhaxqU1uhlv3rmWJcfMFjg7hV2usQ8HXKEYUjjiHXxfsCf1KmViDXIJ3ta25snHtImj96RWgaJWAPXStuusieE0UQFh/hvrTfwD/nMK78twynMgszz7mkFuupQ88pu+1LpdDjT6baIN5Wt3ZGn2SvsY34bC8DocKHeRqmdt0cX7eJh2XJu8lKS/EIcBXg73T8OmkvP0RiNWEFqCCVGt7yg85eVdT3D3zSe+ehfLrN1b58mv4E28vFI+irarbKf1ZO6AFPQphbkfUVjZMuyTCiN6GymDp1Si+8GVhviyO4F/OgzUggLqlb1D6dGRVQKlUn49v+sZIDpRWPAH4TRIjcHgLR2/A2sECvRWJa+KOnKbiqCDg9c2eehVdbkuUGtlKpIZs9yN9hc6t+uxjDk+T0e+ING9W6Dehx/Ok1LyWI+/dQ8RqQcEdFMJJRmIfV2PelvmhnmP0saz/gP0+XvpDagvx6io0STGPKIhyBAqiTEFnMqJ16IysHHmrcauk0sQJdtJ73VLxlJvpOAKjPPGAVR69LzWx06uyKHxIO/vyqzQZPsIsM/8ukSLWpE5JQafohWFZwEIhbdsE0AMpHAoK3ZKXp0trqApba+2eDJRObZRLINnA2LdsK5Oyskh50skpBKIzzChtWzvkvjtQqe34MsWSpFJ9PpAFc4SGaovktjPKnvzQvWlS604yAAGpdU1cfd8i8HDIlvX+OgFRe8RqPsldR1UHQ+uFWtqofdMdq9as3RVLiC+EiXYBo9QRTJYsZCdCFqKKf4ZmGCCv/LMo9Tf2eHjMlJxzTi+Ss083yfc/2+WDMRYI9SJxuZNvgwRcuJgjwL6femI6SrGGH7kFNw25vATWBmAXbDPIsNdtsug/s/zym765tlqtSp63HvICH8EVhBkdz71a+274w1XLSCwySqf2RjnyUINceJ5PBuxfBpATkXET02XL1vD3v/wmMK23VBbkTOstz9qK9dha+t4INb9NK5vcfYtZrrmiTOw2jikVDyG1xLC6fAwsO6/k7dQjwD37NGr57n+7NtdlbxPy7HohxP9e8zeLoXyOz134RNzlVsNUthp+zWQS4tiWpR+if0OFuHa4TybvfULWW4xGGL3ulhOPLcTHIH/97ZBXh8Pb6DNBIADasTz6S7/xOlavVc0x3JIxyJmnWlC4onIL554pOGxoZSUrHjKYYhQgWhhUMsic+Xb4/y0YixYIFrmqVd++faVHD9gug+j111+XJk2axBqS8v0PP/wgJ554Yvm1ixYtks6dO+u6V7to4sSJMnbs2JB7Nm/eLL/99luFdrzy76JSfERef1fk0sE2ue5Ks5x3psqLcDnTt15XsSvqPPz0q0PeH125mzNmeWX9hlAAmwDnlciXuMYW+WKlSrvy9f77WqUrnHS9eprk4bsr+O4T9LRUakZf8GXdjmi5xym7Ae6lg1zd9+0z5b9fUl+I6zvW6+BIXV+CMJOLcDZ+D/1Qo5/CEAe7X3qGTGnarrx4Q133m88flr9DXtq5LWQbys2xyrQpRukLyNLEbVDJMFr9fVBzxVk1yShz5zPICbW2Ac1w/2P8NRinWn+boVdic77HI9lZ4bQqHK76OMXsL0YSeh9j1GNpYgYpKTXhIGKXef+Y5ZMv3IoQ2radboLQew888EBJS0uTk08+WY4++mjlUa1bt5aWLVVL38qVK0MEMP+9YcMG5Tvex/s1evbZZ+XLL7+UgoICWbZsWfnf+/TpI9TGSfy+bdu2yu9sh+1pdNBBB4nND8u6bt06adWqFXgQOOvv2bNHli9frlz+33//yfvvv69YByjYqf2rZBSu32OPtMtN17jlyMOIFqdrY8UMM2CsMgbVqtVWydtd8VCr5sPTarP4P33th85j5X8dcahZTjtRPVy1beORZk1V1LX6CN4SixcVv+fcvP9hplx/RxEsNKH8ThZz+uv5O+W5nVv1HOlouW0cLw+S8fp6oYmTsQc133fmjK3zeVyOKMT5wm+iiVHJXUme88sZiLh9M29HSPnHvN1e+IXrzfRUae2rW7RbwRg5YL9AtPgvX1epuVq4SS0I4vWYZfFSu9xxP0oh/qaBf2iaIq7AgCgYzzvvPLnwwgvlqKOOknTUDQ+mjz76SD7/nMYlke3bt8tff/1V/vWbb74pr7zyivLvrl27ytKlgdrfFLxz5sypNNYFCxaU/60sKOhn3LhxctddNGCptH79euUAQfr4448V4WyxqFHin376qWRnZ8sBBxyg/Js/L7nkEuX3b7/9Vq699lrZtm0bzPjw8+8uky8mlcn4r4xy6qBMGfGmW5o0KhOD0aNgBUQ6mKqHo8oHpM4dIwvpAftVGm7DH2qIA5u2eBR3UDCplgv1yJ0oe0hVus8dYmIRaofHvpmLST2J1gOqN1Iiq3XuHtkqazAnUQMVCoFz/I/iF6/7IAxt/XQGqIm5kq/TC5+wRQ4agI2vHkI41oN3p8IQDFKIQ9fr79jkjxkQaj+VKAA2iLEvv46C++6771a06quvvrr87++++64UFxfL7bffXv43arlTpjBWU6RNmzYhzzr22GNRZENdvxXN6yeccILk5ubK6tWrQ0zh1113nfJ3kvaTv1OLv//++8vbz8zMDHkWzfIaOZ2BgxSF+4wZM5RDSPv27eWkk05SDgC0ADzzzDPy/PPPK7f5UNJ08vdF0qKrQS4+P0327eOVO29y4SCTqoGL9W/lVndEnWDhaYk9TIfwrO6jot5PybzSn10Q40GeK884+9FRk76s0f7UVuPJo44mYMQZYjurUMo+RVNRI9f+17SlXJWhbmjJQFz8g7etk+kozxl4EQwoGpImG5diw/PnTydDXxv6QA6oGrf28ixZZpX3Rlvlg0+cYSLNfTJ48GB58MEHFQ23UaNGISykQKf2TKH8xx9/SL9+/ZTvKdRLAKFKMiFKLCcnJy7WM6iNAn3atGnKfTSBx+sT5/PZD43Ydy2w7pFHHpGnn35asrKyhIeKzz77rFxj5/U7d+6UN954Q0aN+kAZn0a8vxFM7XfcZJQrLvJI61ZqnSmVl7FcFHGxoOHihHPAKE8Odchjz3BNBObqhIwsGdU09KCZ8EfraPA5YIG8iaqQsaBWobnOeuCO+4966uXnkreGqo7xapfUG02cA2psbry80L2JwC9RV9QnAOw4w5EljXXiR8fBzypdyg3sFESozwgR4gKTpFsmTrahclDkAKgqPbDhpmpxgL7B3bst8G+b5NPxZuS4u2TBIqKiBY5g7dq1E2q/vXv3lkGDBil+Zpqad+zYEaI9UzDSXH3++eeHmNQdDofwU1Vim5oZvKpt0N/OTzi6+OKLFQFOn/hVV11V/ixGtK9atUq6desmjz32mOLnZ3DcJ598Ilu2bFGsEzvzSuXh/xmhoafJRefa5byzXMi35mG1QYhXda5q477SMqt8Oq4CrGySqIHUwjd7dRUe9TU35/5RXwQ4571eCfG17k0LMabZsYT4fzC55CEwqgmDpmpj9et4xqHACu8KbWxZaWl5n5hju2qNjpsbLqklDhgQp2CRKd/b5bW3vTJ9JnNl1SIuFOD0a59xxhly5JFHyumnny7NmzdX+kWt+IknnhD6n0855RTF3EztmjR7Npdr6tE+++wj/Nxzzz0hnadJnVH1Q4YMkZtvvln23XdfGTBggHKgYUAdA+/y85lO6ZW/ZpfgY5Dh71vk3DPSgD9ulKxMzWSfLG9m6s1NTfXY4zHK0hWhCgXDi9LKy+fV1JNjt8ty018CrEcHlTVu3mj6xo15Oi5NjUtSuhRpOBZni30i/h6wAYa7CAvvJZhekom6mazSAtCiwZWimEj19zz6FRlYVO+mKpnYr6MvRpk4xSEDj7HKBVcWQ4AzYI3nfxVh7pxzzpF58+YpwWDXXHNNuQBnwwxQoxBntDi1cS2yXMdDo15CEzaFpkYbN26U0aNHK58ff/yx0r001/O7qVOnhnzHw8XatWur2x3lfvrQKcTfe+89Of7440ULqGMA3n333Sdbt26Vyy+/3O+X5+HHI/8tA8TuCwXStocZLglgJvya7o9ST0iXGhpJKAdCD1es3nYPkPLqmpRYZX3nPue/G1fWD2e4n+lJYgxJ3BLoLu26LJV1f6BFVQ0KQ0TOOigtXfHjZCbBKZJd5CJ8aM82GQW4STUgSiX21bkrHT/1p+kkjpt7S0vh88Q5+rn/GFEy1SiPPmOVFStLpbRMMyf6JCMjQwnoon+Y5mMthWvNmjWKD1vzY+/evVvRvq+44grp2ZMF9/QRBSLXAnPGtXQz3jl06FDlsLBkyRIZP368ovWTvv/+e6U/JPaNVFio5mqzfzxAsC+0FkyYMKG8E/TVM+iOkee8XwtK4wU///wzwFfc0qtXr0oBdpFGQbM5DwqMkn/xxRfLL+Mhh4F4TG9bsWKF4jNn8J6W4mbAQZUrPyvDgprzZnn8wWLp0NYo+3SLtUPr270jcz14/qvblr65Ta2rOC9Gue62TMR+7EbXg/YnAOH83qaTdDTVHYAWI1Su2rVFvsvPi1nzBM6hH+EIH5Ra/I/e23qn3nnSDNy1YqrZM1FTeRVqAycNQYpfmJFdqTvcxEd8UK+8HknDcrUj3KDoViEetFX2FDjgs82U48904JMmJ55tlLMvcaJASyEEODVvL/zbVsWHTW2X/l76vSnAGQRGwcSAsuBIcwpzCt54BPjIkSMVfzKFqpbGpTEuLy9PeFCgvzo4h5u/U3hrArwUrhmNqKVTGPO7in5uRqRrbdJnrxGj0ZkGxz5wTBybHmrRooUStR4swOlSoI+c7fzvf/+TTp06KWlyPKiQj0cccYSYgclN/uYXlsnMOUVy0jkiJ5xtVubi25+ylbnZU5Ambg8jodU5U/PKq0eBtiLA8FWv+ZS/W0n0dJvg2qucUXA8YotaGMMgItXiqPlWrkfaZKxCPLjMeUCPPoF0i1rsY00+qt5JhxUla4mH+zs+vWIxzptkdohmqLDWAwFQi4M2X75AK1ZR+0uyzsZibq18Hx9P1A0/9J6Fi23IZ1b/tngJimB8rUKgMjVKpYDWQZMwA7qY102hU5FoPv7zzz+VP1900UW6OUAkNh4AaG7WiNopwVPuuOOOcmAW7Tv6lfmpSIwSV/3NKlFgamb1+fPnR4xOZzpbOJo1a5ZyGKFgpwAPHtMvv/yi5JDTNN6xY8eYY128eLGicfNZjz76qJx22mlKJD7v5Yd9nzRpkvDw8vXXGhCAT9ZtcOLjgok9MHdXX2qTVi3VeenQ1iRXXMIg4ypo0AAR8iEs6Mnn1Mz13ByT3HYDS4pWoa2YHEjtC379w4I5CMVL51vTymSUNJ1QwDXBAfZhckmhLCnTFWheOnDgQd/+viSAmVATfartNuPbBWu7d1V8XjtD2+PX+dbT7xGxIAoHfgRSIz5rSmCLun9t2QPigN26c7OMh1komKzAev/1W+SMHxAK6VlF9tTBbQb5c5ZDDjqQLgE9WNx6umiQ735Kl9VxuHK//cEkU/8Itb643R5o2JFzlqlFU6sksAl/avnZ7CGFGzVYCncSQVkef/xxReumtmuM4aqhuZnQqGyD1//666+y//77K21Rc6UmzAh1vXjpFbkWLMSrkmKmtcfDBNPNgvuipZiRH5deeqkMHz68PFgv0uwRZIb+d/688sory/lDAU9rAM3stBbw+7feekvJdX/nnXeCkOAqt8wAwTR79Uy5hUUl0qKZTSZ+YpaBtfKO1TUsip73K3AND79PDc1CahkzMALvby5Kxc5t2wX5vHUnRrhvPoy0MrohWcI4ClETIjRht/hGn/xX1ztNnCzfp0/PDev+Xc9ahhGFOKc7DxvGLmxQjZIg1UzLO74kM1cmFO5WfKHamiQC1oZN1duo6mop7t6DAh+/2uXuh71y3dUZctfNRSgeEig3Wp1+kT833Q3NGZkGVSUVhT1U29bMzQxGa9q0qRxyyCHlzbMgyMKFCxWN+8MPP5Szzz5bAXAh8VqiqeklppdRMNInTfN8MAhLIlLE9PYj1nU8jFRElKMG3qxZM0VDb9y4sa6DBtPsKroG+Gy2xfV+4403Kul4BLfReHrWWWcpeeavvfaa0k3CvgYH4RE9rKiYayDWKMJ875elTZvY5JXnbXLgARqmfRXa0nlLmdMkS5ZbpHd3QvpWfd3qfFzCLpvwtQo/qxFZ1wJCvC4FuNoXg3xTlB8SRxRh0N5j+u0/7Jd/5iaMJ8nSUL0U4j/8+z0Mo/IrPpcqsxyBFsIE80VxvlyTRMAvnfFiZKFudj4OGFqZD+roL7/hlXNPT60TfH6BVS65Ng0pWWoO9QOPOaHRZchj99NkWV2N3CeHHVwmp5/kkEnf0EKhb0OkIMnJCY09oGDph+AxblH0Q1MoRSJqpdS2afql0KUWrYco/EeMGKEIbWr09F/TjMwAM0371tNOslzTpUsXueWWWxT3Ak34mtWBgXM0wTM4TsuBj9Vn3sMoe8K20n3wwgsvlN9y3HHHKb8zF53EWABG2VPoM3iOcK+RqAwWFrYdTNnZWYAN9SHgD2sS5nSjwSzffGGWA/alG6IqJ4FYo9O+NyLmwiRPPp8uzw4rlWcfz5Q7by4WizlUOOptrTavmzEzTdYGFZ+h9Zw13W/MDgUuqs0+ca6o+IyHAM+DNU3HzLk6du36rzQI8dqdpmo+bTruH4xPRBWWG8E8CHIfhHjdGYRCR9kEVoH7c5vJg9tDC9Vv2eaG6dgaVMO4mtyp8dtxQv4BJmLFfK0KWB8E92fjSuXKi03Svm11hbhIZoZLPn6vULJaM8Ap0F4w+EjFYTLS+4Ybbohr9MQtZ2EQEjVkts/grdtuu03JlY5FNGUzzYwmaBID4fbbbz/l91QU4MHjpaAORqGjr5wWCn5eeumlkAC/SHwifxgXQI07WIDPnDlTyTEPdkt06NBB+CHRjB+NWLmtYjAe0fOY/kYceAqjgwakSf9+Gr59rJms+vcUOE8B7ezZYUXKWr3/cbfkZtvlmis1LPmqt12Td7oQ0Pb+R2YcVukP10SlQXJwCO1kqcuANnXHnldWhJoTuvaS9e9/MVYNWKlnlCyyK+FsPaPvyT0n/fsNayZGVKs4eCtMhSs79BCjjtDGhHcyQoPTEDl/7bb1UlihlvOTD2XLI/fUtMaQyFEaZMLkdLkKWNm79wRqZu/bJwP+RzcEefUrtHkRnfjFpHS59ja37MlX2yOmtyZ0qzMamtOZysWgMwZbVVXgMgCMaV3EGKe2Sdx0rVJYvP2j31zT/mkxOPzwwyM2odcnzvbYrkYM3IsX5lW7l3ngRGdjURUCvNC3XRViPAAD6f755x8h+h2D/mhqry5R03/11VfRjEGaNnbI0rkeCNPqr8No/fIC5+GO+9PlzREFQfXZDdKhnU3GjLDKwQcWJilaHeoBFFklC9XcfL5AARrGaOxjS5OpLdqLt46C2ugL3wSr2JEbV0ph7AL0rgwxfAZQ68uqu36S8f7q52ck46jQJ3tuBo+OUVPNeK50YSF8VMCqdMlDR9vTpIm/clRwr0Z/QrNRKk2ZD5CxRfLi/1isI5C+M39BsQw60yybtoSH9IxnJoxGH2A7S2ToEzS4qGdS+qmpEWpE8yuFHT/BxT74PTG+GZDGOtk0kwcTtTiabylwKxYGidZHCv1gMy4j2TXTL/2+sQQ472WfWJaUwDHBRGHG8fHz8MMPh3xH3/KYMWOUe+k7DiYGjPHv/ND/TuGoEUFotDb5k7CpGjG3W+MdA83oFohGRKmjoPz999+VAD+NmO62a5f+94yCgjEGPBSQd4yu14j57h988EH5eIILs9Asr/X31ltvVYIDNWIbPGCQbDaTDHvaXOMCnCb0oa9moDBOYYgAt9st8saL5iQW4GpdsuEjbBDglV1VV2Tn1mk5ZyXtDT0sirEe/XPvGnzq6cOjLtwU/rJe+sQ5H2N//Zw70Wh8/odPRMnH5bmO5UmTjI61p8v7Qalm7N7OXW755nuLnHJCBfziJOt7aHd8ctxRpXLoQAtQzvjqqX1ftrIYecBW+WFiBmo2F1dLEyHm9qBji6V7Z6ssXekCRvdWxYz777//Kl2h8Jg+nd4VqVSAhGZtDUGNwi2YmArFIDdCiOqlb775RsmPZoS19kzeS/hRvURzr5ZupoG1aPfedNNNisAlVaxuRoHLEqakilorI8CJKqcRBZxG1HSfe+658n9rpUj5Bx4GtHGwgApN1ERki0WHHnpoyCWMSqf7gVCsTz75ZKzbFbcFtXhaLXgg0wBteCN5q/nI+e+vvvpKTj31VKVNRtFr/eVPWkCYvka69957FcHP7eCUQYiqvyAU7z5mp+K6gLqiWR592ibPv0JzvXb4QeEcg0VGv2VGH5gWpS+WI65HJ+jiXbss8tn4ypkb+0ELP8rqUIR8XRGf/Esx508X7X5/8qRALV9dt6TORfVWiPungDnj1MijVpIYkb9LbsxpLI0BIZgM+dh8OS7OyJEpRQWyxRXQJPbscSFFKg1CPGCaToWl1q4t8ny/TpNjT3fI9L+IiKsK838Xlclxp5vkk/ft0qdndKTc6OP0wTTpknnTLWgvTWbMKlIiyKnFUiAyJ5nCiJo2kceCaeLEiYr2SqooaBm4FQ9Ra+SzGGtB3yshR/v06RO1CfaTJnv61onoRrrggguUYiEUhGeeeWbI/dH8wASeYfAcI+e/+OKLEKHNftCUr0WZBwtqosFRwIUj4sATKIYHE/qngwU4DxTUvHnYiUXU7mn+J9ALg/mILteqVatYtympfVr9cu1iWkWo7WtE4BiNGGzI73gPD2WaP52meaLP8f3u19sub71M4VlzApQWs9vvS5c33tUEONe8CbnoFvl6rBWH2po8QMRkq64LvvrWJvP+ZcR+EEIbpOfVCGhriwDcuiWkrSpV/mKGtHmaStqo7aIrj7xuh1TFp9fdUaqKHY7ntjP3P73ZxLlf0dkXNfrIBNPd/HbdkqaqGcfIiTl96zr5uzhQntSATaB1yzT5Z4ZTGuUGhHs8PKm7aw0A7UiTsy42A8o0OJqcm6pDpoxzY2zVrTFtAERqmvQa6EHakRPanFnR/qj5Bed3J4oHWrlQLZqdplsteO2hhx5SqnxFImqML7/8soJlzsAuVgNj7nQiiClY1NIZaa+BvfAZFGh6gFn09oFWCmrMtGaw/4xYj0aEiWXtdPrbid6mEQPaaA2oKSKADA8wzCzgmvjfw+lyz230Q+sKiIq7W06nWZ5AFPpLbyDoCkWMVEFjAFqeVV4fmiaXX5RfLctT3B2K+waD7NhplvMut8i0P0IFpRl75cIO+0hWHWrhHM5yd5mcs2W97HSjcln0eKaSw3v0ORYAL/UyqI28SCUHa9xLEQJ8m1UMX+DGqEduvmLvFObV8bKsPLzrs0Pzb5lqtmFzCaJF07At0MecSmcwn7RrUyLffuGUY4+kL1zru0/+WUjTukU2bk6Pe45Db/AhWK5UbromDULbrACmUIOkYK1olq7Og+izZnQzc5iD854JvcrUKn6iCXA+m32jpk5fMX3v9H9HIwafUTgHfyiUwhED6LQqacHfxxLgdDtUfAb/rdU1r/gsWjAOPPBAmTt3ri5/N7V4HlyCBTgtBjT987CVqMIwwf3kAYFR8l6vD9C4Fnno7kxUSyuqMSHKPPCnhmYgCr3YD9OrCvDsLKt8MiINNdSTX4DTivDJF+kQ4KEBf3xjT8nMlupHslTn7VPvXUeMD32w2UX1WYCTF/XdnC79GvedNHvnP3QARlSL+Jr9jYhwQyZyD+so2rLismafDrDaVRCN8pMm/+qRfxfydJ9KAlwbnQ/BSk6khVnluDPSZdESzbQusmBxmZxwlk2+HW+Ttq2ro5F75bknClDSMhM1q2kKdMuwYcOUiG6amhNBFERPPfWU0hRTzfQSg720aHIKefp1qSVGqtnNdvl9QUGBYoJmlHvwvP/vf08p5nH6fJm2VlUiX4qKipRiKn/8ocYOBNM11wxRcN8ZbR5s0dCC4eiH11LmeF/wOGP1ib56Btbxw6psdEkkingAYYQ+26Ypu2f3NHn0Pk2IxjTDxtkNvo8Gee7lNPnfi6GWJqPRIh++Y5NTT0x+E7o6aCMOIWqdgGBiJs/56TliqeO9h5y+d+cW5WAWg7ztM3MmrS3YHeu6lP4+FSVBXAw/88DTuk2cpYAxR4Tbo6C0YYF+0KytHIG63slCFNWP5G2VDwApGEwOh11m/WKSXvsEhGCy9FlPP3jSz9ttlXMusSKPnHmzWqCeQfbtmykTxzilXVtnNbQlVH5zmeWFVx3yyP+K0b4bpmSDEqDGYCm9MKYUnIT9JOY3/dYDBw5UhkdwE/rLGT3NVKrgCmPhxk9hwoA3BqtRC+U9kWjTpk2KsP7uu++UgC5GzQciwhEU5TeeqUBA6iZLPzCFOXOs6YvXKFqKGaPyf/rpJ8UXzmdqz6DLJpjUbVI1O3OcjCm4/vrry4PrKo6DWjt90bQS3HnnneVBZZHGS17yQ3M8U/gYU0Bi8BpN4IxMZ14/LR6EZY2HeGBSg9yM0hVBjyPfNMthB4X6eONpL/K1ahDb7fdlIJq7AAVatHQskzRrYgEanFkuPKcmnpuY3oe2YpC3R2XKzXcXY02o41COJ9gjj03PlNGo/FjXtBIm9NM3r1YQN2OQ84yBR58/aebUSbEuTOXv670Q90/OSPyM6HDUEIheat5Gzk/LjB0qUYszvgGFOA5ft1xc0MYD2MBGOf6oLER2M2e85oJzanqYO3baZNBZdgTPBEfvGqVTBwSn/eCR5s1CCy7E2x+X2ywvvgaEuGcKxeV/4alNsnqWlubFqGZN+2MBE5YM1YhCmsKOvmRGuwdX5YqnLzQXU2BS2D744IOVhDhN6/RZM0WMpnqtNGfFZzgcFmnaSMUuyi9wS56Sex/QRqjdE8xm8uTJijk/WIgz2E07hBBt7oEHHlCKkVSkNi0zYIoP/JWlV7duD/WL0lTP9DEKVvIomDgWBpYRS52xAiw1SpN7vETLCQMNtXrpDNpjRTUS50uLRue/aS4PzpfnAYKHLh42SkvLJCfbJjN/MUu3zjUhSA1S5rTA/50Oy0++H+ddnZN0HLY/HWmT005MHWwHH3LaO/SxyfoNAMHyH94owB14B8YgL/xAWAfrmt6D6/OJ7Zv17Hx7rjp7cNeRX45lSkK9pXpvTufMdbS0/2K1a+2F+DXsCqS1mhnYw/K2y4VI7XIrUerJQS0AwWrBS+QOCd7wyYrVbpyUTdhwU1eIN2nslPEfG+QyQLP+8Ze2wXpR8rAIJSgz5LsvM6RpkzIxGauWAkhIy/vv3AOgmXQZ9nqpeLxuRbOm+ZoCmcKZwVaMviZ17949ZNKffvppxR9MEzKFf1WJAWv0f1O7ZuUujaj9Urgy2ItCJ0Dq+rPBh9umlVluvV49a3fpDFjY41V877/n4aAzM1227zTC4lAGy4Nb0WiZE0/hrUZiB4haLX3XTMdi2paaxw69GwLZjM8lg23St5dHrrzULZnpAZS9DZus8sVXmTJ+oldmz3Uqz2G/aU0gyhq1ZPqztVrqDHTj31kUhilvVRHg7DUPPLRgMF6AzwvOHNDiCbTRBVduY5AT0eK0FDS73Yp1VHMC3OmyAUrVLs8Mo6AOBMoRVvedV+wwodc8GlxV12Xl+wyIt3HI+o2adUy9gqvv4LQMGWhFznjiHlbllmLq34GW8+q7ANfmp8rMTJUbB/Ua1PuHRShcDItgtD43AYzgFJw26z59ItBLvjTv4uT5vx1bxBMiyAHEMMwgN1ydukJc2yIKilDh7BiPLF4arFkCnRm41vfcmg4ft6rJMB+8KuSDF++V4Si+8mCBYlonUbOmr1yvaT2e5xJi9ZhjjpEmTZpEvI0mc2qrvDZA3C6NcvThNuTOG+FHRdAKDiIGg7ZtkQeaoGAZTTUl0uezynW3mWTcxFKg1lEA+xSNnKTlyjP6m3ClwX71fr3T5M6bLHLJBS48Q71PbT94q6apGKq5j9C2SH0cYkbucOVqesGafqRB07TNGALmm9cUjRo1SjmkqKLHKCcdD+z+cWX4V9UOgpH6SV4sWGSTU841IyCztHxd8XoHDg6ff5gmJw+quQj4xPPPgAOhVU49zyKz5obObzsI73Et20s7QELXZW44x0yEuC5rlkgZrC0xDhTOtrbMF9eXFTyUeF4lV4vJo3LWIF8at2u6GwNdGusRO5GT/VtZdfKVYz0h/u+5FZ0NE38PACyEkk9ee9uMhcx8zVT2ivgkI71Evpsgsl9fRqfTOMTx4CX1OeWVtwrk6Rc4dm4gVVuusGPIzdcWovCKXSl4wfZpUmelLPpeE0VEBKOPmXneBDWpSDTzUogyIIwgJKoA55hM0r2rQ5573IFYB59M+rRMPhtZLFZLEfpLAUR8bfUTIBau5d/g7zcUy7uvFcr7b1ikZQvyyqgIb02A8x5GaWsCvEljG4BOMhFE6JLLLizA/SVKO5UFOO9UBbvB4FT68tZLxTJtilWOPDQLFhKuPXVOOB7GHBBnPhwxJoCALSxoQu09kdkCfB7N7jyUMXedZMA6uuT8DPCR5W8TKcDVQ828f9PlxHN8yBah1hrwgWdkWOTNl6wAcmGRn6odOhO1HuNrxwA/uBkCPHT/Y0rZxVm50saovZfxtZroq9chIj1UmYn4BM9hxx0zNtHPT8b2Unn3j4ufDjFdglCN93FTRNR+MuOZZq3lsvTspBKL7NdnqLZ2x9YNIWM2w9T+wdt2uei86iGexcXIGrvYAN+rVT79Ik3ueqgYvkUtD54IVybk9iI16LYSVH2qup+ch4Anns1CClAh4gvUjZcAMPRT0/xZXaIvmoKKbWloY1qbDB6jSZvCLEAGCGqrvPo8tbZSpOBVF8PbAACdNHnuJaN8Op6bcUUhQvO5Rb782I7qb/orv4XjCwXZ0y9kwpRcgniDQDYBXQ+MAWDqGE31mqWD6WN0J9BPTZM3TfvBroXq8J4HFNZlD/j4DTLomEwZN9qJLIXq8jS0Zx6vRW66K12+/bEUuAcct8Zjg5xxCiqT3eSRIw5JvYDTP2cBQe58BpyqFhmNcrGWF7btljT74dOoHT4cbs9YZv1MsaB2ouvE6qyrVLl3rxHih7bt33v6+jkE1A6NxKkwUxZEMc/BomU1sWSiec5SOXXT6grABkbkXGegiEKpNEfqVn0gCofPkKN62fVF4nYH4GUZld2hPfyb403StQs1x6ppOWz/iecgfJ4jiI5qOib4CEFR+vfvX85CapQsCkKo0oogJkyhYpEVEgOsNBQ4apf0oz/77LMhU0G/Lv/GSHN/rC+Kb5jkqktt8uj9PphfEwm/aZAfp6bLqYPhv3YGb8gGBFpZZfI4O7ToxJh5eSjauClNXn/XIC+/6UTuu1ZWU91iqXFrxUs0hhAhj6A4wRC3TNnj33gAoH+9IhHvnIh74arP0f9NyFhVgDN63wRh6sBBBRYMWA4SQ9S+jfInSnK+hHLxX37FjAeOUc0B59o84tA0+XGSG4fMxB4aEtP/aK3gTUIw2xXXG+WjsaEHZCO08GeatZLLHNk1340YT6Cg2oyYlpt3bJIZRZXdORVud3Vs2uKD1du3XFvnHa+FDuw1QvyCI862f/bbl9+Dp0dE4ysX7oct2skxCHBLJuL2ePX2DfJjIf3DGtFvbJG5vyE1q0/VNdRkGif7QkH71TeZcsk1xaiiFHw4QQlERBq/9EyaXHBOoaTZq2YmdblRfOJdB3y7bpk1Rw0UY4oWK58RxIW+bAoGauiM8qaWxxxmEsFZmJdNHzCJQodCqCIRo5v502yHICoBYBYztLUMeegeJ4pvaL7oRM6Aau79E0Fv519RBn+tyj/CfX420i7HH6NVzIqly+jtE33yFuD6W+SZlywyaUopAhNDBRn5SWhWwqxquO/BrZPHPAAx0JD8pFlcI6a1kX/8yWI0Gs2aNUvefPNNZb5Y3EVJI+tklfFjbNKlYxnWRqLeB4Ns3mKTDz+zwYJThop2TvA3+ABpkiGXZcorz5XikJSoZ+rlffWv4+Fk1pxMOeS4onLrlNZqexyqfm3RQaxJEOjLVT3HVSanbayoyITlQcm9V1/fZ+j7b6+sPoeSv4W9RohzKhpJ+tm7pIi7cUTgXzLkPPiAXmkcNQauTmb2p9IiuWLLuqBUMxVg4tbrMpCLqppPq6qhVnVAwX5qdTFVTUMOfb6q+bz0Ribybp0QCsG4x6q29eDdDrn/jmL405lXQC7E81xV0K1ajUCewQb5b1nAD3jEEYcrKVLEBKfmR2hV4n1r6U3sJ0tZ0v9NxDbNfBzcf4KnUENkpLgWr2CxwO/dxS7/e8QoRx1WAgSvqvQ71ixxXOqaIF0yJAvIWxTaAmuNQy44N3ykNO/SgUEd8eGcKz6Dz547H4VLRhpRS94L4ReqCaenO5QDEPPBL7zwQiF+u8PhUFwMNLdTeFND14B0+EBaOSiktRKuPByR/zTNr1q1WumT1Yqynm0z5P03vXLoQXQtVXcd0s/PlE6TrFhllYefsiBoMLjYhnoAYmzBM49aUamvFOl0jCmIZw3Gmsva+N4gu3bb5MBjzOAlrQuB/mfAVXdf46YyJB3VymqjKzGewTV6L0zpHwMzIwbMKltagk/PJOh2rXRhrxLibS0tDljv2jIFnG0WjbudbXb5onk7aY6FnExUiJKAd+/aIl/n7w55sVq3tClpNL17JNIsq3fkjFzG//0rKdF41EXFVrngSmCrw8Ol5a2qPTPC74no6pvp/9TM6/FvNytX22X8V1ZUm3Ii35eavRo8xpQmlg2lsNGKhkTjCDVJpjoRp50pYyoBRAhQrAcfaJFrrzBBiDLYqXoCM/qsMGIdhxz1VAMUPLsceDR8tIciWvqDMhwcoLGGY5FyQyIFkEFWrbXJiNE2HMJcCB70+CFIQ7HKTzrppHIAFwbFMcUv3Ab99ttvK+VRmaanWUBUPlhwiDPJXTeb5fEHEpcDzgPe+o12xE+YZdTHDFwLjdhnQF+zpshkGWdAMGa42AO9705dXqceZGmRuvVe8k51XWnALpfkNJLnc5onhQAnl7zY+87YtkHmoJZEDPLtk93mf//t2RC7Kk+sllLk+71KiHNOIHK+wCsZqMkYbqJgUp/WupN0s6jAGslEvwEe9goURikNwc0GXvNDgBm9p3bBX0pKTTL2S7odVAFA0JzLLoBANSSusAS1PK/HKsej/vjU34MDhih4jGJHXei3AHV5+sml0iinKnEBqvY65vM0CB2D/Do99BlMiaJJnGlRFctrcszMI2eZzXvuucdf5lJ7pdSCF++9apbB56gR5okVlJVX5aRvspD/HZp6M2mKSU48jvWzI89J0yZeRFMnOitDtaaIzyzf/mRBsB3gWP+MdsiMdQAL3qpgi0HMyiWD0+XRe10o6sII9OquObV9roVxExxy76M+FNOheTyAJqhyHIFtQ9Ll9Reg8SNivzoWjLrdV4yyZh2CYq9GNbDZqktJeYf5VsGtMbddV2mKgNJkoR9KC+VqFDzREZle1r9Dj/PnrFnyVbL0vab7sdcJcYjlq2HkQ3iKRJXQF6A06cu5zfxn05qeBv3tc2s8e/t6+QuaX2DbQ9BXOzsQ3LzwC9akX47+T1SBejFdvpjohplTkNsdrAEZUFI0XRHmuTlmeeBON8zSPlQp4yZbPW1vT74FAtYh197qQhQ7zbTBm7YJ5Vkz5PYb3HLsUYRrrYqv3ABQGKvc/UiafP1NqWzbEdDKOTsEH6lYv5t/J/BIKPKZSTq2s8H3bJM7bnLKPl0DG6T+Wa58JWE9KTDydptl9hzVQrR6LQ4w7wc06GUrSoOqZul/msNuApCMlsIIvzTAZVq3cgM5z4O/q8Fq1RWShNldv9EqE742Q2i4ZccukbnzNCHIg0c0IUwXipriRKtC8+Zmefhut/TuSQtMdYU3R2dE4JwFEed2YJ/7ZAnWtMtdsV2zdO5gQ9lcVN3rUwILS/WfGzxD4QsaVZ/vkVYBn3fooEz5c9YeZX41oiPh/qYt5fqM3KQqrBGHEN/N11X/6k/9K/c6IX5I0/16zdg+j8AvUYsZH5ORJWOAExxLP6iLJTC5pEBuQrqZsr2WA8AY5d7bkWv8GHygNTSrHq8B5sVMueEOoJ95NI2vIn5SwAXBrbd5cxMEuxnBPyJnnlIE/yU5VhWuqprdPwts8t5oo7z9PtLQYGILkBnIYwBKOcIuY2E6zs2uipakPmM+nvHOKMBMji1EIBtKqOjcr4GyCcSzDCCsuYHVrYGnVMVMrU6gy+WDiV+UoLFrAHrDYi67sEXNnVemcFD1QwfzsiJQi97VyZYCWhfnjdShvUW6dDICNc4irw3l3ohI+jTEYiup4fHOoV8z93dp1y6WpFUr8f3wC/G6cdiJUFKya2eHPP+E2qfDD3HCquC3/FRTgPvgAyoqRl7+Nxny2luiINKpfuFQPjrsBmQRpMs5Z7ilc0cEI1bruf65xWtTVqby0Aff+8XXZGKthb5L2Vkm4L3zffYgUI/pgVXhe/g1wDFfcJUTzwxNKctAENt/HXuIMXp5T70LK2HXXb5zo/xcAFjb6P0iQ+fhE0gzSVgPkrehGtruk3fAx/Y6vNXPi37/Ej1Uq1lEoM42+PMgxPskoUmdL9jx29bJwhIEowQtaiKc7VprlpysmkhzMQCHHHWYHw3nA9RAWKILrMMPcchVl1jk8guhmVfZFKkKg2GvZ8jIj1yyZJlm8gxMZP/91OfccBW+w3M0Q2m8q5LP+Wy8A1XjgBX+ClG5wguuAftZkectSBlzoQJbvGlNqo2CgpNR3tS9Rn9igynXI3/97ZLvf4q3PY4yHlAcvT56NWDupiEOadOaB0bw1cBASs3qEa9Qj3c2EnM955QId/8to7/bKC++TktJuFOaETn8ZnnwrjS59soSadm8Kq4arc8B1LvPvrTJ0uVelN8VmThZjx9fMXDLlZekSXvUHnn43qrDEGu98flsctbFyCT4JvT5zMwZ2aKtDLJnJIbZCWzl8M2rZDWAmWIIcefFJ582eMw3X09M4KOTvqm9Toj7Z+RK/GT0UcTINRM482zT1nJxkgG/sP/cEp5FlObriNYMDQQyys3XOOS1FxJjZqy4eleutskLr1sgPEv9OcGqwLjoXIeUlPpkwuRgH2K4ta9iddP0f/ct2JguLoZWFQcSckiTRtmwyS6PP2sE3nPFYBdqi6gg1dQuj91HV4MTfuGquhkoXA1IdaMJoYJwVFVhsVjc8M1XLt0Y++03wB1hk9+mm6W4xCSPPatilpeUEJ9c88XGJxytiIK/8lKaxvXdt2ChT2bMCi1wEr3fTGtEznm6RXp0NePgoixIWFrKYAmpihsjNpcSdcWOXVYIboc8OdQFV5DLr/mGO3ga5dwz0mTI5QY54ZjqBK4ZZNMWK9IlbTLtd4NM+bFMeWYA/0DfHKnjZyAnIvm/cCEeoCoHO7UVmtGH3Jwho8YgUDTIksU5vT6niTyIDyB6EsXyhLQzLH+HvLJrux5/+NbHbr271xOvvRha9jEhvUjeRpJrtmqJT9mSceweKRyHx0X0nZiwqPdNc8gkYKkb43nXamkMW7weOX7TKtkJn2yADNAEbTLjR4EJtKpCK9oAVI3i52kObAKE7uTmb5TDD6ZQF2iOan2ZdRuM8ua7bgCBuGVnnta/AHCLqncaYPrOgN/cK/v3c8HnrMF+xsNAgIV6jDL01Sx5H+hcq9fSzMzJCtWsmjVlCcp0wK66geDlkfbtAjzTbxqN9apUXCSh5mNlA4U7YtESQuUaZeSHFvlvhQc88spCpa56JFI1sZCnY2327ola8/imSWPgy98WOAiZzQQAUjWs2D02yNp16MdyHlA4P0Z55kX4h/Pd0HgEfcUa8lt61NEFz2HwqjPIcUdnAqvAgGAz5r4L+hfqztDP53jmv/K1Gp68+o1BVq82S2ExfOhPGrEWvTiwVNZ+tfKrVivhb+0IEDXKCceWYK3E65JR59zlMsrSZRb5Z5FZXn/H68ciCLeJBLswNOgYteehV8ONgQp2E/DOHX+0ludfFT4ZEFyYLoOvZPpf6MEtG8hsXwIfvYc5uYJ5mYh5PzJyxuzJizVgLs5Z+Bwc68L69n2s97y+jVcZzxn9T285ac5X9Iv3jjRAmpayoDXOatdNMpJQiLPfz+3eJq/n7Qh64dUAoBuvSZc3XthdY3MXulFyq6TQrCy0Zs2xw3RokFffMsl/S0ukuLSiSdKMu4xIwbIC29wMAJd8xUQbL/FgsXmLRab8YJdHnnIjKA1pQRWKxahGFyMOOSYUGDFC2Jikb28PkNOAT14DpzSXywT/taoRz/vHAhhUamCAQ0UxDh40VCO6ko2M/0Z2ulvMJmmUy8ORQe6/C7/neIBhLnLxYGpjAV5pL7Ladjw8VA8JGmlLnRXyPhlnlZWrTfLOSNVHvH1nSRBoTcVZ4lyqJndqdayK1qG9UW4coh4wmjYuBp/j6Ve8q0C9fucuBw52BlR5s8jnX7qBXueTzVvpxyZnOLqKlh/EbTRNRz9NOHj45KzT1EBElYfxvfjFJVa4d6xKJP74Sa6gA2W4+TVI41wbIHoDgrxFCwAB3ahe+/wrJoxF7WuZ0yP997XJjxOL/O9H1fhY5jTLoDPT5bcZPDRq6HpqbMVFwMZ4IQmxMXZAWdlv/XJUIIw5Ztex+w645uf5s0dXbeWk7l17pRDndKWL5RXEoN6qvK8RiF/cgwj122FiSkZiBmuPtUuVBa5uN+qG3LKlRaYiwaJ715rwjWvPCeaIttmFZyWF7Ngv7fLyGzgqz9Uiy0M3SOKjvzY0A8AZJdK6ZfwakNYbRnGfcBY2vKlsI3JaFw8PghiCZx+zAAUOPYT/5OrLaL2ouHEHfMZ+67nC43A0aUqabN2m3r9qjQklQqntqKAusQWCxjs12OvA/hbkIIu0b2tCOVU17U2/cI5H+MTaAvwAMgi+uuth+pLdiOLWNtRAdbXI75C6Joc+ZZdMnIYtFgPcKIxV0PoYfKDR95ap86AeGEh79hiwvlQN8qmhHpiw3X5TcSQ+8D4z4G6NcumFVhn+UhkORqEBXrHnK7ivatbGJdc6gP3PA2R4oc1nkpuHH2KTHqh6+/A9bmQBhLogAnPMnH+V/llolwwHMgWqkXnCg/e3PzrklPPUNakROXGwI0PGwuJoSrJgNvYxjqj0klsvG3Loax+OmKdvFdWfq2K9wfVnpBVG0k6aHrZOthOG1RFtkOfghPoyTqjJBfui9pgv+ZgilCnduV3yPcEahgE+5yxsnDi5VyotWVdTCnSoPJQ5nGOVF14T+eW30M1E7ZVRBvaHif0uL+owF8P3F/P0HXYwTEfbut2Cjd0MIBc3ItorB78FblRfAWqPXTpVXgrNmoSaq0uRG//I0+E15/UbVZ9ngGIJU1UQZWSY5dgj1Gp099wGJKImbmncyAsNPNmCxhjNbZJNm+kSMMlDTxpkx06fTPsjViyEwmF1hmFG6NwxwOfjjzLJoGN1hv8HcXbSFDNq0Ku8ZhT/mnWaSyIaz1VcgROOtQHtT+VzJ0C0xiewg5ecQbZsA9TrJLu8+rYP6G5I+wzJmFDHbcQB9bSTEJ9xP+F9kXbZ1KMC78Sp6Vf9zWXsRbqcfC5z30NTHu1INXineVs5PslgprX97c6dm+Xzgt16UNoW4B4ce/c+2muFeHtjy95rvZt/xpRHRW9jQZRF7feRjJgexrpZPLQEn759ncxGUYDg7ctqsQCGMk0uPr86PrREj0ldbkXFFpkz34qiCz7kDpfC/BkqrKklH3JQmnzwlg8bvgq5Gh/SmbasgXu9FaZsIGs9i/zf4iIPTPoVBUbAEB15tBU171iHi2htGpQcejM0/3PPtMOF4Abmtk/235eCkAbp4LZjHQISPT/62gt4241SVARgkH9QmOYnM8BySmFuh0lbiYOoHCOgts7xBW87anxE/CMNWEgCvQ7YSoJHku6A1p1mQpqYVQ7YzyMDD9BwC8K1EZ0HGsywzwvL0TvpMuJDJ2IHNNcG2wuMLRfm8r49rajA55RDD64Y8xH/iPXNTsWrWODEKPc8nI7iLaGV69jTjsBHn96iIxAXk08UrHGXyRmboWohCDEGuVrbst/aWLYHR+C9j5Jv5mp3DqbhcUdGe6QFi3sB8iazauudq8L4/3SWyODNa5X0i0AKhhHVqtJQjrFMmkLjSEZiqs89j6SjAhZxm2F29pcHVftqAFCKA8FzFgS/0fxanfxcphURLMYiM/9GWsIH0NzWaj5Lv7Fb0aBiCWc9XPSX3/Tv54rZHmO5+VqbtGqptn/5RV5oY5gTJUUrOedGz0iDr1HASmByL4RQHz4C5SsXG+FTV7Xc8opf4Emg9na8T4h1PYP/6CJR1w5/v+0GmzRv5kVQo8ghAyEIlDVUvTmmu2brNoDCDIMQf7dEqXkfTEzzzM6yQtM3ynVX+vA7U/FiCqFYg6vG9wbJ22OTxu3hYghaa7Q89VLSaNtKF3PEUhLVeG71b12Myo3HbVylp6HCa84855D3Jo6nNr7X0V4txBGlfhGi1D/ArEctiHIcgF8+TFLgF65YyotLt2+UqUX5lQK63n3VIddcnpz1jbnx+6AlFBTakCoGHOd3iqGVB5sZ1XSmM09JU1KZTj1BT15tuHc4NOjO40E+Np77x59m+fpbdVOf9odL5v1b0RQe6+RW2Td+xCFpCEJS+9Ao1yT33aGmA5lM0MTK/cDq91UJnkreHSqUx+Qvg+NIv/5hVQqi7N6D3GykNgUofk04dPwBv/iA/dNQ/ISC3Ctnnw63zAHOSjyvHr/VrXL4iDQgFjK6W4vbCGjfDCp99P40eehuJwLWAq6Q6h4cqjPnq9fa5VIEjU6fWTkn/KmmLeRKFDhJRjJAIXmlYJc8v3Ornu6txkWd9FxYH6/Zq4V4N0fXfsuKl//C/Tba5PaHv+gT+I0yVaiqpCNO4o/EVN+iauPBdPjBGaghXSZZGXWpDcRimSoARozOgG/RDfNkZYztpqgYNfwlG9KnSmGOrg7wRvi+rEBFs43w9Wo09TfCcEb31V57hdEPSxpos1N7TxUAX2Lxpz58bwCWALI95iqQfcrJcwTS7JYhzS6Ytm/3yup1oXnQLHLScx//fUEXH3MEcOGPV9d1u9Ze6di+Ov7t6DxeusKOOuKo//7MHgVuOEDMmTdLr31sCJI0QeMv8mMGJMecvT0qS25Etb+KFpDTMnLkNcCr2pLWTeiTgVtWy1pCJkYnT58m7W5csGOdVnUo1vX17vu9WoifeeDZpomzvvwOs4oSEZGJTPoE0ZtHpiVXjfHgHhfAHMx8ygmocBa6xVjkS+SXnnlKdUAramvdszSiVa680Sy/Iw0mb3fwgYSzYEJOul0+es8lbVq6oWnFnwYUfZZDORcr0zqynz6WBp8Iftbkq1uT/Q/0O7iMrcaRVast8vf80DDSRlAWjzsquBytenVl/iey3/7I93wj4jdsiDyn9k3pHer+aIm0sMfutcu1V1W9kl4iVkPlNghQZJD+Rzhk+UqiDQb6TQyMSa07yv4WFdchGekPKCVXoWpZYUjAbtielpx91KD+X077geVH90qqyZ0gVRh6Ozr6PD6Vj/pBI7gDqWb3ItUskdtEohkUvsKZQdq1sckXH5pkwP4awEMyj0Llym8zMuS0872SX0hNKxTQxmCwYDxpyOnVgvaSfzyJnmstzS041eqTzx3ILdbv8z30IAbUBWu96r11af5NPJ+q0qJqGZr2RxqghgWugIpuHDPqyJvl2sutgGUtg9+96ghqVeldrHvUw5FJrr4pDe4LVjYMEN1Tx6Vnygi4B5PTE6729WNk3dy/fUssmFVeSnt7i1g8qc/f7/VC/OQeJ/T6Zsn3UzHJTaNNdC+7Q34ColEs7awuFwtF2fnAVJ9RIVKd2/IF56TLx9BgjcbqB/fUxhi5EW3eYkcQmk2efI6R98G+cpgwHVbp1iUNdbJLq5U/WxtjSewzGG1sRrlMNS961CciS5Zg5vEmb9nqRLqVfiGenW2BmwVxCbi3kVJ1Ts1pH3SMs4plXRM70rpqbe16GwS3Xe59rEwKCyua6I3AyXcAZtYkZ56KcqS1UGI2fj4Y4bZwyLGnO9H/UNdTD+xjU1q0EzsKnSQreXHQOHjjStnojImV7urRosXbS7ZsId7HXkt7vRA/Y8Dp3SbN/moSVsA+0VZBOtDb3m3WVo7BS5DMel8eEI5Ogm98XVmoL4lRs5uXOYAnnkwpZ7HfO6eL1a4y5bTBJchJ5oakCSl16XZolwaca6s8jcIsVku41KbYz0juK1StkEFhhYUAfnnMBvOoR2bPCw4QCx6B3tUZ6dVH1PI+DhySRM453SQXnucGtKsLmqenngXiVZ51txvvyFYUB7nEJHPmMR0rOPAOCI6oD3/2GQ4ZPqwQVcWSN8bEhXFcdp0dxXtCXWic8ZdQ4ORCFDihoExWQniuHAiUtkKPJ5YmXnbrBVce+Npno/5N1rHURr+S9zhWG6PHMyDAl+HH70HSIeyTS5AAuyskBaqWOhjnYxoh+O4yANRUJIJQ/O8FIkul1pRbUVxk4AH5MuMHpgxlKIVNVFI32DUIghr2OvxnN1mBQc6YBTWlqz6QF7nIq9amyx0PpMmxp1mkfS8XEMEKIcC1bANNyAT/1DvycPfyb15Z9F8pynKWyv2PFyvPvPAqq9yJPuzJT0P2QDIbYfWOPYwA91iR921XxjtnHs3ngXgLA7TWtq3T5FuAB418swACPLnTApctpwAPRR+kGb0bcsKPsKYlZU548IyMQHGnfEQPxqhYxlsK0pvk7rW+cI1n9WO3q/q7q915I34B4jGCNSMQsdRPz8yRVxq3gPM8udlGvOGLtq6XRWXMY9U0MzV39pF70+WJB6nF6dXYqs/c6reg8psa6cdj4ef7WGTq79omFdCWbFYLULHscufNpWKzahutfvNy9ftZnRZUmE2OlAA1oz+xyAwgkk3+gRCiFaPkKx7EtPWIqltAI9uvb+y5/fhzj2zYqLVbMdWL7VUOGiQ0bveuRpSStcgRhwCuc2Ag2EztQarwWl1LGs2akyYXXCkoBsMAMG0M6vcGeI6fetgO3zdM5+X53rH5W52VUJ17Oa4zBqfJ19+HIrOZcLh/oWkrudCRlfRv/kuozvhi3vZYbPCmi/GzIvFeHOvC+v59ckujWuL+6f1P2++rOV9PweNaRhPijOpc2L67ZCa5EOcYFgLt6OSNq4Nw1dWREUDl12/dgJxMfJpW7UyXUSnveM2tNkC4lsHETrNmsJAzSv/9MuTOm4xy4TlwHRiSW2tSeYaq3C6L/DkbBTSWmuT1dz1IswvWtkM5q1TdgkA9aIBVUPIaZm+zDBygmnc7tsPcNo09t4uXpiE/Xy1Zsm6DoNqWuhVs3yGoaub0HxwipdgZUFPcJsccYZOrL3VjTaGQTBOY2+sU1CS+1UfQlvkL7LBsmGUstNZ1G0J93wye3KebTUa9yYpspXAvpMY6mjM/XY47wwX3SyDYjjN7RW4TeSqnWQTU//h4V5NXr/aUyblb1stmZ8w17NyvfZcH5q1dQeVrr6YGIc4FftpVzUZ/PXIUztcnR1oNZBTdSE80aSlXZ+Qqm1/ynsdFsA3LbcAd/gopZ6H9hJBAoZGbr6U2njqaU0Uxxn/PnmuDwLPJR59plgVtpEb4L81yyolWefx+L6ppOeEvVytxJQ8pKwpVwqw4lJjl6WEi3/8UbF0I9f2rGOsmadXcKqefTE3YCcxxJywO4QRtwPqyc5cFefXuMBXEwr/6GzdbZO58o0yYYpPpf7oVmNoNG4OBTTQO8n5VW91/XzuK1gBL/S4PCns4JRPlXuODya3NWWF8gUnueDBdJn1TInl5Wh14zQ4i4DPw/Z+0w6pRVqO554keNQ8mJ52dLt//Qn9+YF2kQwv/sU1n6WBKflfIdKSWDQ6DdxGGVyV3X3NThxffe3NbovmYau01CHH/jDWX7LO3yp5P8c+oqWb0Nz8LQW6EmTqZI9U5rF/xQty4bb3kIUAkQAZU7SIcqxG5t3zZU5vKnEZ57BnWN0cJ0u0VI4mpadrkrlutctkFHunTM1mQ6wwo62mRkR/Z5fHn3P6iKeE1DwYkEkzkpqvN0qcXSkaez3xk1Xcdi7btQH7zELvccr1bTkNBmXgOMVq5WeZtP/eyTd7/EK4ZRTBEBsAhrwefY0N9eC8K8LCueLzV6GKNqHrfs9LYlO/t8v7HJpk4ufIhlhaOAfvb5Y6bDBhHsuV9xx77n7My5LjTXTh40SqjpQtCM8nIlveato7dQB1fQWF04fYN8mtRQcyCJw4x/lIs3mPruMtJ8fgGIe6fhqO6HdJv2rIZrDEetSCKHVHqv7buLO1MrOSU/HTz9k0yoWhPJd/4cUdbZMLHKL6Rnmwaarw8VaO3Z/4NrfwdBH6No6jSxsQZUrXFltBgn3ncDWQvgRk42N9bk7MY/HoBJR31xD8Z55VlKy0y/H1gWucFC272SfPTEj7UgJrhjGEwA77Vh6pmmnlUK90Zu98jP06XITc75WhUSJvwiQvWiXgqZ/lLkFJse4yoQGeF5cOA1LYSmTHLjAh5Pj9YoAf6T4tV08Z2WHvc0h7m/UsvUOFQQw8Rsfsf70oIXB/K9/kLjCjn6ZH3PnAAuMUppWXBJWrVQMimTUzyKeZk4AFqpTE1dSxVCL0FxO0FV6Fq3yTa4AIxDi0tKLXapLUMtLO2fXLTVgC7XLh1nSwtK/OPIWJ/nT3bdnxl8frV9yX3iGqndw1CPJTPqMItp0VjPaM8J7fuBLQjW0oI8SJEpQ+Gj2leKauPBxOQqH7NlP36MeUslTasyLPj9RoRWZ0mpw82oOQioSYra6tZGRY59uh0ef4JJyqkwcxcqY504l48pSgIBPOatRa57X6brFrtQv8i478Te7tdWwf65gXMqFt692DxjNgad7geF5ewrrod5TppojfK79/a5bCDExPQuHGTDch6FkStm2X1mmLAqTK/PBJ6ngEWkHQ58jCz3HWzC/XR1cOIwVBzh0eN7+vWA4zlSav8NK3Yb6WpyCkD0udsCNSzyw1Xcz1oYEiJWwO10RLHu2ZdhnTuRw02dL2cn9NYXgVQVbJbDcmnabAcXgxTeiAYNyL3aELMrA3epsIzGoR40Cx1sXY4fYVzDXS5yCZ1CvETM7NlZONWKSHEOcGjoIk/BI089OUwyNmnZcnYD4pQFjMVgnb0vU7crJYstSlgKC8i9aywiKbF4AgG1RdNM/WQyxzy6H1OuBfckpGeiNrdatsFhYQNNciHn9pkwWKvfDQWvuXiin5l7dXzIWjKrNQUf+IBm5x/donkZlenL6plYtKULDnr4t3oB49uZhwIHDL39yIEwiXiwKZlC+BA+51DwZx/8MkS2bPHiVKkmm85+MioarvZWRaADqkpgnfc5JbWLXwYd3C+dVW1c7U/hUUsbGOQLybZYJnxyOcTPbB2aKbl4LZxXDJT+7bLN18YZd/ekYMI9a26ur2KQvy089Nkyg8VoJWxV/3WppN0NSe/wsEZvDdvq3yE9LIYxIlcjE/vWBfuLd83CPGgmR7U/eh+Pyyd+i3+FDFKnQzrarPLW/Ax9YA2ngq01euWm3Zskr+KoY0rvnwSBRk2u5+N8APy5a9fREFWVOSQYW8Y5XUUVdmZF1zzWRsrku7Ag6wss9x2PVliRMW3MpQMVQVLbPjRgMl5yVKrfD4BLhaU4/zfUFXb9PlY7jSc0FSDwuiDve+ONKTE0VzuRF9iFnvQMUnEArBKVhuWBQ3MK9MLP3grQy69sEi3T13Hw/yXGJHTizzrt20IgvPJS28wVSv6QYR8t1gAXnMHDjywNjRrYpQbhxCZL3C4Cc//4GppPqSFWeWDT9AG8A9efN0jJSVqSdvwJU/ZNv3eiJO42SznnVWWIJ7r51RNXMlKZSecbYSLQ7UkKByEAO9rc8iY5m2kMbAVqno8qon+VmxTOfpiXzoGWvhiaOMxyHvqgKMumzx72phYF+4t3zcI8aCZvuj4wV3G/jh2FLbdw6ItAPr8Xm3WRs5FzmWq0FbkGh+6brkQtCbwQhtRazlNfv8uNKc0VcYUvZ/c7FWtb+lyRLB/apZPx5fJ6rUVBSXqf3Prw38M+E+XznZxwH149OGI9B0UHZVrEzTQl4czElsAhEKBEhRYhz+qps2K26cRqWFpcseNJumG1CyazE0m1YeZCLcGUcfufyJDXnmzEOmFwRYWg+zbJxPaOAO2gn3CiZltlddIlXMbZPGSNLnvUS/qWHsV0JhQ5DP1eVqdde3pNjty0LuoMaXkBhHjHn8glHfk8/wFFvn488C4irB0V63256v7DS7hTPttW1ukRzerXHiuWY47ukxat1LjAxLB88RwsOqtvDMqQ66/Q6v8pwpx4lo82KSF3IBMmlSgD2EtfHzHZinF/hSDSs4bdMZB436YtFejtAXzqEGIV1gx0K2vxlaM7NDIwC9k2kN4QW7MjFrBNNZirNXvKaQey9sm7+ftCBErrWFzWL9ECzyq1S7V8sMM0FRsiE5GSdMRHlmxSt34VbtEzI2jCn1VDweknBwLEL/MKNhilkMOdEOIl0pWZk24MAyydEWm9DiA8Q+VDxA2q1k+fNch551JzO+aeH4omwgVO2uuHfXEzTC7uxGn4JL8fDzXz5jwh5wqsDrklgDfM+Gi6NDBIiccY5YrLymBEE+uQiXVHam6fmFJO8qHgL3go7lIa5tNfmzVUbKSPjNc5cKw/B3y8s5tet7Evb7gScV10yDEK3Bkv8x99plX8N9U/DlqZZxmiPqc36ZLIt7DWmtjVGGePLx9c4gQz8owyPcTHXLQAfGlINVapxP+IINs2GyVESis8tffIj/8AtOvLyawRNy9oKuCwvvWa0VJDTv7dFVT0rzJcTcY8waDrFhtUyKUVdzvcGSQ4xHU9+n7XpjvY5otYz5R3wXaiI0AVUmTfxeZ5PmXVT91ZHeDvpbDjhB8t9ngprjNjMI4XkT460/Jq/pT6+pOgE8tscmgs5woFhQ4iPJIPqx5a7kgBdDZyDkerS5D4aY/KhVuqsRXnjyn43NUXXE8GZ8bWrg3GXtYy31q0719/ry//9sSS4jT7LMYqGg9ETSSKrQP+toCh4/NroDQyi/0yV+zDRDiqTKK6vbTh1rkZTDVOsXpMiEAyi5jPrcqaVTvf0hfrpY6FQD/iP1E1WzvsBvgc1YBNW4cYpBOHVwImNN4XfNeyTFj7VEEOHvlkx+nFspNd6fLZyP9tufYg6vmFVoEhgdBbUUy+GwDqqUxPdMgI0any7IVXgQisvRssJasJ/hOw9CHpSMbed1nq3y/62aDtGjuksyM8Gb8ag4m6W5fuBhFW7aEWhiyzCbpYrYmtR88mJFOuJ3+KtF1qHRfecqZD4+aMjHp5qEuO9SgiYfhfobYry6U0nfxVcRqIfziYZjUr08hkzqHeh5OvNNx4g2m+27PkmcfZ8CTns2zLpdrTTybmOX4IDBq5Wr1TPvMMJv8PU9flapclPB8/3XVv2o2+1BVTRXaNZlCFY4LEyZnyEVIk1JzoKPPY0a6TaZOMcsB+9at9UXxo4PvewpMgHvl7+pB4+Z7bECxi8z/Jo3M8u6rge+tVp+0a1M3fK+JFam3zdIyu3Tqy8proe8zC5382rJTygjxoQW75PWdW5WCJzGOuoxKh12rgYI50KCJh1kPdsncBCHOHS4j0nLhYptcmC/XZDUSJS4pBSg4rje4uy+96ZRnHrP4BU8KDCShXaSJG3oh8pa7dlIFw6g3440SD7cAamdR8ABSWGiVd0YB+a0sFMzFguCmXLNFdrhdIRWhCovc0IIR6NXdIulpiXcl6J0eJfockek5WW58And9/6Ue/kfib+3wXe8Ya/K6giKzbNkWOn/Uys5Iz67Jxya0bToBNsOiqWPWPJ0atfp61a5NCX1+fWgstepS1hLHjzr42Gl41MpYj1uImt3lRcJiXZwE39OEeYyD5VsqGmB0vEJJ0P+a64IaHR74cGuJ51Px/trkp0Huftgs3/+s1VoPPLt7mkP+BbqgA9jZoeSTdz8oleHv2muOpbpaDsc3LdAwFv8j3avrwfXioqee0zIggobD1DKrXY9QrHMecBda63HJ53t269HCPYceccgXdd7pJOxAgxAPMylpuTbaI5fHmi9moz6KsnmpRAfbkD/V4ERJpSmL0leDfPtDmoz9khaEgPDm9DaxWOQRInXhH8+hBGU64IIDxKAyj7zwuhNgNCxNGfxdPWFNvR6GQYpLLEiX5CBD531/HNwO4TueEuSTf1zQwvWdeUs+mvgFQlEbqCIHGoR4mDXx0Tejne2kOX3iMe1623GSTC2qrYCm1OJK6vXWKOO/ypLLr3MjRz2Qn67lCJ+ZkSOHW9OUALJz7RkyML1iAV0f/NAoV3uOV3aiGEsDpQ4H6ELZuh0Ibd/T4xda3CgNmrgDoEWpQAYI79eR8qoW9IlO8PvOj3XN3vp9asx2HcyO0WphPmLUMl9cev/BpL4BwP2ppdyG9tbr8coPPxNoI7VGUQfLIkkeCW8yENJuuNMjOxRY0WAyyJEQ2I/mNCn/I7Xx13KbS1+7A77/UGfKhs1lMvJjRos3aONJMrk6uqEc1fyZFIHLCUJ1Fg5vsUWijkfUwiUL4AunEqSjv65Deu0/tha6lJKPaBDiEaZtjXMDEYHmRppVxSMHO9BKZ5lsSiFtPJyY9ng9Mm16TQCepOQ7kdSdphbm8drknEvMsmNnKFY25zbHbJYPgCZoDjqQURtvBOjNy7MRhMmdPiDe8ZtL7kdmwp0PZDYI8qSe+dDOPfhE5Yp03MxPSosYi5t0o1uMVNedbl2gQ85+++33Y9INIEk61CDEo0xElmR8jq+jh+9CkL+6Z5eC/ZsKtA/yxE9Mz1I0sgZKPQ4UIBL9prvTZOIU4uCHorJlQYA/3ri5INMtLJ0H8I/78L2tQqAbD6NvvFcgo8ekpx5D9tIee8JkETZHJkLoIS25mbMRFkw9ajhGse31j99fkdyjqbveNQjxKLw/tN/hM/F1Xqzp4WmyROdqjNVWTX+PRDJJazCb1zSba6T94hKr3HavXd4ZuQfth0pqBq4NRQDb+cg+iEQ0mN+Snis9EPxU8QjndnshyN3AIW8IdKuRyUtgo8XFJhR6qdzguRnZqM+ZOofz9/K2V3IJhGGT5+CufR5LIPvqXVMNQjzKlH77z7cL8TVh/qLSorJi+RmfBmrgQE1xgGb0a29LR8UuhmlUdn2cmpYlpyGALRZ5sce/3aildEAlvtDtnvjbCHQ734tKZA2BbrH4WJffT/qGNQBixtzWZRdjPns6YDhYjEkHubr32/d3HdfttZc0CPEYUw/thSXvor4x1Ilml6aKLh5+wIwUrRpRFMTzqdpT9ua7mE506bUOpJIVgA2hPkRWq9rfkS53N2qqsChQyjMyx9rC7DocWjuRvULJg4pvJXLREJa15Hepo9XtXesj1I3CWTJjHfTAwSwViP1d4CqVMn0uyL8/+OKjNakwrrrqYwNiWwzON5fGazaJEkEU8Q0hXOC7u3fIQ9lNlJcp9cgn6zeK5BdYUF0rNOc41lhWoejGhs36zoJt23ikowJLWuUTQ6zu1LPvDVJQiCIq96YB3z28Bn4QBPi7TVorgWvxUD+LXT5q0V4OR3laF9Yv17BKHvnjzxI56VyH/DgxTTq2V2tUN1DycoDxLXbEOZzK0sj6BGOdDmYjSuSOLMjTs6pcPVu2nbF48/o67W+yP7xBiMeYof59Dly+acG323BZ1LqjDA7yQH6nJkN9MmZcsdx8HfKJD2DEDDft0MOIx2NR9ocfp9rkp6mBqJrf/vTJ3HmETYy90Q/sb5dDBrJgDDUJI4qQeCUtzS0mI2pyG0NNa2ruqC5zW7K/Y1XonwqQ6/WaEDlOEzo18NBIJmrgna02ealR87gFuNahVhD8J2VkyeSCPeV4dep3yLpAje4Lr4Ign5QuGRmsBBauNnoVhlZvbmGKV/UO7FVd414vUwIrU+w3sO6ZT46xUO4mly58De+xRwx6c/HY9+u+40ncg9SUObXI0K8XfMsd9Gt8uimSJwq9SG08RzVrph5pMJfsOYaJwhR5u43y3mjmj3vl1bd9snUrczphlKA09+9faoS0PmE7c06JzJoTYOGrb6m/n326TQ7YT6RzR5FzTleTAXzA1FYFx95JPp9FzrvMJBMnVzahkyMD0tKhSbeTjGrs3EbcO7xxK2lsMsuo3TuVlMkAeWXmnGLZ73CHfIcSop07UZDvjQVywq8/HrLU96Tq65M13w1Y5/GRUe5/TC3lmqr0PALadFoMijOaNiZeRwNF4UCDENexPExi+tsjHsJiRcUzZL44xRwjwFOR8vPNMKXaZcJkk3w81iluj0/y8mjGDbNTVWnzor4eEASE/iR9McmFj4jVapIb71TNwicPcsjVl9H/65VO7X3SqpXmC1Yy9EOyoFOR1+H7rMYWTPjaIdfd4UUeOEujhm7WTCHqYrPJh9UU4MHPfzSnmZJX/h4OoQGzOq9QNfIDjjLLHTdmyIN3F4rFXJ818mDsMC3OQ2TPHhPgaUPP78Pfs8rPv/ldQ1V6F0T2RQWyR+4NbMHpDqPs3y+4GAjXuda4+lP9b+XDVNdKgYrJ+lZgB9B3/vDmiuOLZ98YGlpnNVmHVYf9Sk1pU8sMO3PgWe0nzpzwMx7bOdqjTfBLzW7bRVoYk/ts9MjubTKykuaFGn89HLJoCd+ZZNioVVQqblu9e9qhpau/X3GhAf1UBTrgwVH6M7Dp6YFvrOWlE8fjDLJjl1Vm/GWTq28qAxJb+L3rUJi/h8GE3s6U2AjyUlhUHkQdgPF78uAjD7fLmuSx+9Pl2svLpFXL+hTXoG6BpaUmxIUE3ttX3rLJxs2qa2nHDqSozKwY25qId0Rb4+oyycowydFHcF7xd0SaXnC2Sfrv65T0dBxiW2hwFQZp08OOvgViFeha4aHuWHt6dQwDcazVql3K93Op2ymDt6yTbTCnxzj7OA/s1vv6WcsWjqra0/aeuxqEuP65/gSXXhjtcr5M/0ON8SsycvW3WgdXboXF4IANK3EirrhZa8sh9PXSs0iUayIF9aG5WD7z8C908JO136mpq79nZxnlgnMo3NV/33KdSM99VBxx9S/6jvyhU1BFtSqueQzlKCFPP/rULq+85ZN5/3KzDkXj0q7uB9jUMc3bSm6cQWx6u8ZN9nFo4yOokfOmSvWdTdK+rVk+fs8ihx6k+cmVC/U+ooav07dStdWRn2+R+x6j4PbK1m0GAOgE812LDdG6XHGMiRpzxT4H/1s12XdoZ5YTjqVgN8gbL3ilQ29JWSE+w1kq52xcrWcdFOGi2DmTelqq59foWfX1nAX6hjegUZ+jZ+9aMAVXRzSpE5X6bAAuvI70nWSmLUBKGrBhOYS4vo2IhxOFglbLSY5syTCpf+B/L0Nd9TbwrYajtahn/TGiUTX6o7hINmtQtf4uKEbyakbW5ubYxWpRzfEtmpvlzpsDZkc74unOO4vaVOUxs//aX2sjgEv1p6pa2NjxNnnmRZMsh9m6tDR8ZkA6kNhOAx76nYi3aFPDVh4n5uDlgl3ybdEeWV7GClMV+WWAxmiTs06zyYg3SsVkYt2ARGil1X9jAnwNbeufBTb5d5FqDv/kC5PM/0e15Hix/rfvTKXoe4M0b+pQ+uwNOoCniiZuxFo6b8dG+b0wP+Zkt0jLmrylJP+0mBc2XJCizts6mLhD2vbvO2P9nB/w6ObRHp8NQfZWizZyDCpIMTQrGSmWENd6zZ9MmTtcqYBlkIsys6UjcoxJnczWKvv+N0KAF8Jky/bfKtit4CevQt7oGgqNCgzTd8zQbgpo5ZpgLtffzUbp2Z2R8QF69nHAVCIyXouW5zcHDSiFhh8Jzzm+3gSeFLoOZszKQB62V156Q2TRf2XCAjSq77uyBSQbAvx5HApPg6m0NvO2mQZ0Mcyey1Hgp/KowWesi9490uT6qyxy9mklODQ5K/lvE7/2w71P6t+oXU/9LV2cOAeVlRnk0afZa9USs3WbW7ZtV6OhK48lvmC9mnqj9a8sHlIrZyqkgjl9Pd77i7atl5WlMYFq3GccM+jmSb/88E7i11D9azG5nbdJxO/WHdotkPVziOAWVYjvgZabD2Bj/S9lEg0SXWHgVAYgPPshUObU9Gyx4N/nI/80kZtX6yB/7suorkX6B0J8IYrJkG8ToQUugvAgEdWJeczKBhxTUw+Yz0PDgWCgdnugjYWmtZxyXjDvVc34nNPt0qRJeH/z3bf4pHmz+OfrqaFm5OAHNt7xk0oRtBY9H5/a1TE4PF2QmSun1IGvszU0/jeatZbLtq5XDlmuENcL+AwGL1xcKDffjfmanI7odYc8eJdIy+ZlCH7TTNHVfQtCg8mcLpOUOSnE1L//8ptZvv1R46tBRn+iWTPin6NId6g13zAOzIeNnwq489ejWlxjne4N7WD5bXGBzAViWTC5sbaLCYhOq1clN0bwlfEdOhLHieq39DXGvRoHdR1Utk+P3h9BiOu4tOGSRO7NewM378Qgn8MnalTRxTmNZRgifr1JCvwSSRNvi7zjG3IayRXA1yapmw434tpbJtpGx/KZpO9KCuU/+NGYiTOmcLdsROWjmqXIWYQGQ9XOvGoUfrBAi+6rb4EiNZejpORNuU3EosQT1C2NLMqTR7ZviXKIUnlG/px9ml369PJKDyRknn8W3ZpV631xiUFeeC20IMvM2VgPPwfPPywYIUF4VYmBiMxbK97fWxs1w9rDGDDEgVaHHAzceY00lMN43w7FdRR0E3+ly+lL5OvzXfvHVSI/6DA5a/1IBXM634DLtq2TaUWFelbEBlzetm5Xfeo8Pd71lzojq4GentzruJ7fLPrpJzTdMlrzbZECNLtlp+QV4jCVDli/QtmUrdAsDkP5wuFNWiK8CsVRkvTgQX6XEFmMhlPsgnfs3qpYPEjboCkuLQtTEcI/SaFpUzWwMBLQpBJ3gM8BEBJPsva3JdT0n4BHVLkJikZaRC7YsUHmIZ6BFIun8AKIiupqkDNPdshlF1X2rZeVmuXCIfSPVhb0NLoUqY9KCCnsDXMYJd8PcWQo3zSFq+g5oC6WJzDijw6DsRaPsOpQGbft9MerfFG8BwfZIikA/+dTe/dr6cFWqVQQ4jx6dV2zpNyqFmVSXY3F/uJOKX0wIRO/FzRSNdViL2BMuCE2atu02LxIGBYTVYjT/Pg9CqIcBzNoMp6SmBPcw54mPax2uQhlSQ+C/75q+lLtLgT1gKHsxvJuoxblD9+CeuhLnX6QGHz5Yv52KQ1KRl0BTb5MX7GF2h2Q/2mEzOwF4X13VhM5EG4MCo5kmg/q2eno44gmrWQyTKJjoDEuhUCJ1keWiS4kxACu+vjzUsDGVrZwQFSFFeA1MQk5iFVphTgOhYwGuRmBmLkGHltFDse7oL2n1UVhS0TfiTNhQR9JV8Aiw08BLA5zYYqe6SyRcbBIbdBnlk5EdxLSxli4yOgy0EGe40444eOx30/ScWnDJeRAMsqYpJ6ZHLGfsltKx6GTEaPUeTJ+qmkLudJvlk7GASn1z9FPXa9VMg6gQp9CFnLQZsG/f4MDVQEEvUIY8PD8HbIK/neNuHF7Im0wUf2T8TFG6aPf0qF4dvH7E7CAtISAOdHmgIlVHUUyzwl7yBiF8aWFMLFvUjT0iLwrZ0+0baZ6ow3mKR/HhAlN4+6OQ+o1WXANESAHWvb+wIsPdCnQp+r1IL41UJ2rlSMsOrvW65Jv4GZ6ZucWCEZ1E0/2wLYngE3xTh4S7mNQupi+KxLPSbGua/g+aCk3MCM+DvRv3rfnnK3/RjWpc3NuBHvi/LbdhGkVDVS3HAjdrg1SDK0mODwoH/9+A+A34fLKfykplvUJ8sMPBFRqdyDUsD+DEbDWGZphhmKuZeRBap2n2ecCrO0xhXvko/xdsho8ih14mJh1oJ51VH41h3A+EUVgNBoCc3hTBJrxW5oZ08BfjerLm8ix0a20G58Xd22XyUX58jIyGJIV7KUY6+Tq7evlV/jDY5CrY+OWr63euRnhkg2klwOptXPoHVXNX/crHnFEpMdQiNNE+hvQ21rBZNdAdc+BWOF5kTb4bdDgixNkim+MqP9Mv1CpLy8e+bZD4ZFb7gQm9jYgcqkRyBq8T8BQHXsVaDq0NhsGYcomfdXB9FhuM+ng/5sdZudghMSKfA20FPvpqXgFx7cZGTEEAErWeJYtSgyOLlyKklsvvGqf1z4duS4V56Ku+lxf9pLa5h/zF4fgE7UgytnZufJGo6ju89rud8PzGjhQYxyg1YlZ5ZNg6iVtQF7w6Pw89XkxLFJNYaG4LrNRJVdCd1gr9q0Q5Ee3Q33RqmtsMpKkYQqYZ+C+ehMWg1jBkLh0FT5Roa2TZFhJ1Y2GwLYqTEdLaT5hs2y9FLdGLYhCvzMXccOGUwUmN9ySchxgSqUVK/481rX20+1ZjRU/bnUosYlj1elJw73xcoB74HRE1+tYAp5ezTqOXrRtdbyP2Ouvj6pJ7vXcicCAtp07sTzerlj8+b64EID/ZSnm7Yw1qobvGzignwPVFeD6n9RwZTJy4BfkvP/nB26K0T9Pl749GGvUQHFyoEGIx8kwXj5r5Z/z8OOfWLcSgWk1qvU0UAMHGjjQwIG9kQPLkAWiM72zbNJP38zYG3lU3TE3CPEqcrCbrfObuDUqfBijdd9HMYkGauBAAwcaOLC3cYAxEu/s2aWkIMbIXKC1vWGjrOICaRDiVWRcmy7tNuPWmJhSm4F6QeD/BmrgQAMHGjjQwIGwHPBcfPLp9zfwpmocaBDiVeOb/LJoKk3q/EQkHi9XAS1saYLyjKvY1YbbGjjQwIEGDtQ6B8aWFMgOfXtffpsOnf+q9Q7Wkwc2CPHqTeRvuD1q4CUza97P36knOrN6PWm4u4EDDRxo4ECScIBgSrRCxkbzU7bGxc8Pf3lNknQ95brRIMSrMWVnHnDWBNy+J1YTfwH1qyFEPRaXGr5v4EADB+oLB7YBgOaFvG16lBf3ofv0G15fxl0X42gQ4tXgujnTzFPktlhNOBngUeAHvYh1ccP3DRxo4EADB1KcA4tdZQq4i5788N79B/yR4sOt0+43CPFqsP+LqeMWABDybTQRDMVdqUVGZua7o15SjV403NrAgQYONHAguTgwrgDI7jrqRqAkzc/vjBmxPrl6n1q9aRDi1ZwvxJ0zXzxyMWt/+9PLiiR68cZqdqTh9gYONHCggQNJwAFiuS9CQK8OKmua1aRBC9fBqGiXNAjxajIQt/+CDzF/o9K80hIp03EyjdVOw/cNHGjgQAMHkpUDhJnegYInq/RFpXvW5+94LlnHkir9ahDiCZgpFJNkgFtUezn9Q6/uYbnLBmrgQAMHGjhQXzngk2FKWV8d3nCR/PrKhdocV4MQTwC3u2R3o0kIIejRaRtOqCUN2ngsNjV838CBBg6kMAeKfNBnYstwd9fsVm+k8DCTpusNVcwSMBW9+/Vdsuy3pWvQVJ9wzXE9M8jjq/zdcg4qPB1nT9exxhPQsRpoIhFFINXabrFJvSp0N9B7b8XWK/ZbbVVvP6rWh/L+9+0j9nPPqjRgtuqaM1e8kyaX9yX23qc2k4h5ULlbmQdVbzvQlt5xhFsF6vOD6/9Vt0fVnD9/J/WsvRAO9OoptsHnVlpp7I173j/invBVOferw6/Yb1LtXTEDvvA1zqho1FpnPO17dv15+Z+baq9z9fRJ+naxejr4BA/rcbT3ED4RD0ao1Cj3NG4hd2bmilenAElwH6vcHLdR62vDxH7gAVVuQ7uxbM1acQ6+TFi6MhIZO3YQx9uviSk7UNaS15Z8MUGcL74aVx8sRxwqjqFPh97j9cruI44XQ4SsAVWE4H/t20nO2I9C7i15d6Q4R34Ytg/aiAyHHyKGTh0l44ZrxGSziTkzI+z1ntIy8RQWSPGU78Xz70Lx/jxVpDBy6UYfHmC75SZxXHRe9Q+COFjmHXqsGMELjYzHHyOZTz4CGRr/1uD6b5mUUTChXc9XU5Qm4xFOfKKhfVtJe+s1MTfKDeFX4Sefi/e1N8MeOsIxVhH7Bw2UrFeGhnzt3rlLSk8+SzzK8KKMsWULyZrwWcgVJaM+FOc7IyOvWaZUnXCcmJo1lfSbrxeT1SrmrMyw13vLysRdUCgl3/0oHgr0r78V8aZ+Bsuowjx5dMcWPellNKVnx/UiN1wclgMNmniCFkYzyZq5TfIL0VxOxCaxr0wozJc7M7BBxb9HJqinVW/GnJUlaU2bVL0B/53ePXuiV47BddZLL5CMLp0qPct+3dWyefxEMa5eq7sfRmymFfvNGAXrw/eL89kXxFBWWXNQdUFMkslU6V6nI3wZeUVgdWwvlrNOl5wrLxWTwxHSx0opNxCUljS78rFfcQkOdnASfv+TlD7wKCCEIrsLjZnpYk/APPggvCtqlwYcOGxo24C+xbtEFR7j8ELe7jnyMCl9/GkxQFDpJZ/FIrZLL5TM7l1D+ca5uHiw7P76G5HVa/Q2JwYr2kOfgn2G3twccT/1qLifwbyXRo6gNhiNYm3SWMz+wwzntgzzqdkIgjuh/A2HD9MZp0nOjTi0YRwh31dwobFJo90uZnzsGK/gs3vQsVLy8ONiyIuJHaV7/LV9IQ/lLHiiIz/cm2u2Tc1DmeYGqj4HGnzi1eeh0kLfrn0W4seOWM15sVU3lEOJziUfhG7WBeeFvwgbRdpFg8VXBU0xuEEj7s+55AKxhDF3xprDiN83aiTZr70ojW66rrIAh8B0FhWHfDwVzI4UmlknHCvW228Wnzl1z9fkbfaZp4n1lhsgrUy6Tf9eaN+ZV1xaib3kix0C1Xb5xVWyEITMO/iajQOB7ZLBVZ7mSjd2aCtZnPfbbqwkwL0oR1xp3l2VNe7sE48X+923K/xKVSrDEWcrotJ1WF88J5xw/OhUHWey9Tt1d4ok4+RPy6evx4noK2hTt6FrYd9ELu7VMJ9+UZwvg9NTy5JEja0Mvlvv3PlhOZ92/tlihQlSI1cBTMQjPwqrubjy8iCEKzejeUEznn9KjNAIwxFldya03NK3RqB4YfWqF5rQWMYF50renzPFsHxltVYU+57xzmuS1rNHeTucbw+EdxFM764tW8X1wceKtq2ReUB/Sb/6ckk79ihhXxRzMv7XCJpZIdwJBVfdIAYdJlZqPvkjPhBDcUy4gpAxsn/GkB5VZgGvKYRp3Lt6HX4Lvz1zbZj79hLHUYcLBTiJ2kGjqy+T7bPniO/Hn3XxNuvOW8rvD3dDFg5dO95+T3xbYoIkRn0e++Y472wpm/KdGDZv1dW3yBf5JPPpJyStd68Q/7YX814weoy4li4T1xcTQ7z81mOOVGIk0uG60PhFruXi4LonO1tK7rgPwRKpddTn+/x63nYhOmUswqULO3XrMUmmMBakgarLgQYhXl0OBm/KYvgZ59Cr8KecSM3Sz7oqxV5QbSwMxKm4taiCxyfmww4OEeLu/AIpe/VN8RhxRYX3Wt3mwxtrfRnpYqhgKi6FD93eob1yFwWG4u+E2bq6Qpzt2WC6zR75thSedwmEQ9U2dI7EeNVlktYvENdIQ3XBH39K8U13oGBtseIn5nXBpzvfrL+lAP7Qgg7tpNHo98TWvJnKaghCB/hZ0LmjyPIVUVcoTfQ8GBS/O0oMVTjUxDKZc+pKvsLhbervETUs5fAFE3LhQQdKo6H/Ewt8wtqBJGfYs7Kj30HC2tJRiS6KZv7x+y8sXbtObO3aKqZ9jQxYB9UV4sq8d+ksOeM+kfzz4cbYtDlu14HWH/OlF4kDh7FgPhbMnC1F196MScG8e30h5nze5/l5mhT+9oeU7NdPcl4eKtYWzcvHlwGfenHXzmJY/F90fiXZt25M73qAvOggb6ZY5z/z8gvB51kdtzVcEokDDeb0BK6NU/Y/ZREYGlWl41b2YQrni6ubc/Ancsyuch0GXPGeaCw3HrC/pB08MOSSws/GiQ+boSLf+KGQu+ZKqL7p1Z49HgnSWrUUO0yssXWICI9D8F06hLgR/nONylaskrK77hcDgtQowCORAQc6WgGK4OdXfIm4tGT9BiletkJsxx6pe3w82FSem8q8j2cu1IfHbleZFx5Mf58uZbBqBJPJHj5+oOLAjPv2lXQEIAYLw6LPvxQvKmFpRK3Vcc1V4rOHt9LoZpZ/HdlbNBPrZRdVOT7FAPeJ46rLQ+bdjQNnyW33qPPuX7Ph+mVwucU7a47kj/3CP+8+KdmwUUqwFizQ1FONCnxemVS4R0+3ne1at/pJz4UN1+jjQIMmro9Puq5Kb5KxCUL8NxwxqZJZI91UggU/togm9dDIa10PqecXpQ25ImQjd+bni+fXP2RPq1aSww0XxJNnFkyRZRD2vh9/qbrw9fOSgiP9uiHihGnV/clY/Rz22/8tp54kjiBXAhso/BQHjx0EvYil66qPc77+luyEAODVnl9/F8N2lK9VbtV3v/5O1+yVVT0IpQ25MmSkXlgvXL/8KoXQSulf1zhBk31R1y7iW7Co2gPhYTAb6821cJF4JsO0HkeLSpbAlZdIWrvW5XdRtcx7813xbY8ZGlN+j3v4e7JrA9Ks0J7n9xli2IrKXyk476OBla4joI3jdi/cuOaTOFjdcGkMDjRo4glcIh//8JmrhTT6DE1GfYvpN5oNLPXU26ITyKwKTVFbNR52iGTANBm8KEv+nCWGpcvFydSynQHEO+5zafShxjLTRuhy4Yy/hH5LjYwmo2Q/er8Ye+6jf5CUWIgwNvXfL+SeMqRaeab+qr8dXul0iXf8JPFAI/ftQIQvBIyevGTtIYpJnzyM46NbaCmSObZGbjr2aHGcNKh83IopfvqfMQPbzGefIemHHhRyX/Ev08SwbLmUgSfObdvLD2pcGxkvPVeleWd/iuf/EyJsqN3nDn1GTHCF6OYHe4rgS1OPfWBlCdxVhv56mCIYD7Hm9pec90moh7g97nmP51E1dS058EdJocLXGOSDZvNbrIsavo+PAw2aeHz8inm1UUzLcRGdq62iXTyluFBuznZJR1NoOkrMB9TTC7zwnWcgP9kYFJXthFZSMvpjxXzuW7REiqCZWRCQpG2bDgR/lZx2sshk5NjGSTTRG3KyJd0fiMY2zUxxevAeKbkV5tBdOrVopHtlnH5KiAAqhVnZt46FmeISC35BFd895A2N+JlfjGEUnU4uYLPF/wsRDCefj496D90NJpi6BSlXkYhbNw8y6UitM0O4aeRGKmEh4iJ4sIh0IPFiuGk3XycG/7yzrTJosoVvvqM048Nhq+CHnyXn4gsQ/Ke2nAY/eRGeJRO/1jlef1gG+lHA4EwcvNK7dyuPdDfbrGJ/4G4pueUuEZ1atC8tTRxHHl4+xUq/6UqIkhoYjX+6B5KEF25H8GUe0Ch1kLN7mw6/LtiwRselDZfo5UCDENfLKZ3XrZPtedhU5yKJpB9uibjzFSD1BLqXzlbr/2Wm448Te5vAuYebYukfM0Rm/l0e2euCidpzxqnlgoL5uOmILi+oghA3YUMvQhSwCQFldn9gEWVEJkz0ZYfCTI+c5Jh6hX9aKl6nyJooN/syAQACzT82QYTCnQCTQdRLFasEBFs8pGilOVnRAf9xDdvORapY9MrQ2sFDHTSv9cCysHvYa2JA4F60dEDjMUeJrWXLkK6XwvpiREyABgbkpt8Y2Q8ETyFR4DsQyZ0PgRyvJcYIIVsMYW0c9Y442qimcGXeYQFyH3qwOOM4GCg3csj+CWf8RzTyEbhIZ2qkAYGhseY9nvmuqWs59PlAafsvSs590LNLjzj00HELxq6pqe7sle02CPEamXYjcmq8THSO7PSGEJlaUizdMqofpFMjQ6jNRhGolIF0pODAMA/4UwwtTiPuj75/Fkjx1N+QS31c+d8dCIQrgQnX/e0P8fWYyiiCz/IB+mF59QUl1UcxSePTZNhzsn33HgRq4RARkyprztH2cgqd9DEjkYoGU2yMtplNvPPw48SnJw1KMb/rPXb4hU/MsakXsJ+xoF/4ZMZxcd5Kp/0mReMQlAYNOqrQwiEs4+orIJwt5bxgtH0p5j1Y1vkWL5FitJWF2AONZ2mI7C5CBL9P1xyFDtS3ao0UPv282Ie/hnkPjDHj0QdkT95uJSYhFsWau3D35/7wtdgaN4raNPlInXbXMbAwKdac5Ca6waaWqq5BHct5y5tjx6yOdWHD9/FxoEGIx8cvXVcf2fXIeb8sn0q/eNTItekQ4tel5+g+net6eCpeBJN2GsyxwRtj4ccILdi4pZKgy7/9XnEs/BtAaqgdR+ECQcDI8gKYsI1R4EojscUD4b+7cyfJBVCH9nweJhqPGC47DjyiStzUg/StBxFNjWqPLS4ovAspzKD96iG1VaSmrdEnJMIdDYJ7xe+diKgvGDtenDDRG2Fl0qNF+iCI0w8MpGfR3rCb5v21a5UeBj+j+MVXFCFOUg5bmH/b+edI6fwFIsAkiIeUA+FPUyXvozGSe9nF5eYyCyBSc959XXYedmzM5uI4LpW3pcx5BU280gzjD3rWT8wO1tIFmj9cx+O8px125MNf//GrjksbLomHAw1CPB5u6bw2s3mOU5YLE3wr44b622AQyN+lxfKvxyl9zbZ4dCidvUiNy3zAFM9AuljFzc2FACRDHwCnVNgtCYNZDE0vEwApGjElrQgauUyLrUFV5IoBpmrX2yOkBPni6UDN0sgEk60VvtpSRC3HomBho/zeBPCjzHuOAr5CjbOSGR43V9R4Y2nXbIcae9GdSGfblRerq3F/zz7ueuFl4Hv/q9xr6tJRbDBlpzOoyy+QlDHjMGUAqpoh3SEGWDFiCjmkB2bdc3vIAdaDvGo3AxlROKQiGeG3LkAmArMSSHx21skniBNANFXKUIDZwPnMi1KINLHywwHaNHPeb7xOysZ8FhV4RulEkARmgBvHz3x5Jd0uDCk5/eGCv0IgbhUpnjL0Y1mxbNKHe1HaoXvXOdIgxBM+tw1CPOEsFZn0x4RVaJYRQ1Tl7JEesdvtkj2Kv1OfxlUDXa3TJhWN6oD9xAHc6IrUGCZtRRCEcTjT5F1RcNoB11kKQJIqbYCAPy1EUZM0mOmDEbRykANcgiIaUQk+68JxEyQbPluNMhB0VQL/vaBCWcWALvp5C194RYqz4RevMDb7aSdJ5vGxtcDanDTFTI5oe/lrltJdD34WIn/b9+qLkhnk1iBgSc7ll0ghgGtKr74xZhdN/fpK2v77hkyXBdjkTVCwpJKc8092RRhE/jkN6H3FCiJc/JKPwrbonfdxGDgRC1G9n//NRipjSQx3hwEHjuKfcKgYxEOFcvqStFNOlOLnh4ls2hJ2/PkPPwE89wqZp7jPfuIgyQyK6o/JvCS6YAsAXkpixGz4u7v19fdHNJjSa2Du9ETX1MBj63+T7U1tF2OUUWuMc1O8eduG2FpLPWUXzcXp99wRdvvlwuSmzYjkkE+Y7ZrXZiNFyQAfaVVNkfS37zj7QilTcrtVYrvp0VLOuOOjeIoHecbBxPuMdA9EUEd9MP0zL9kD2M+QD3z0yUeqZsjgNH6UYDMAlRTeepfsgStC0yzJCs5TNiK2M4AjHoty7r0jbNSnMu9h5jwcjjGfyZRE01FVc3uwj0RG23bltVLG/Gx/p/msDFh2oh4L4LrwrFgZckgjdK4FfYm0Br2wJFScczfXAVLTUpF2Ae/i4Z2VXV5hxsIKQ9VP7E9FJtVCnxuEeA0xuU+Pvjx17o7VfDFOscvduurvxmoq5b73tm0jRmBFJ4SQAqXma8evkWnP96EUKPOTY5qCy29Qf3EBjrZ446aQXIPcOwC7iYpr8fQmnmsTwrNqNMISriV3PSDFFbH0iaoGM7ftvTcAPhxhboGQZ0A1sYQQ5j2u3P4wD/URHhcCNh7iXDlhvSE0rEbcTHMfAdbATdfrnvdUmvNw/GEgow7yXHbSqa/ouK7hkipwoMGcXgWm6boly0w7+XZ8IvrF2Q6F+LfIGe+atfdFqbN2tV3DCwcvuB3kIT/YB+jJcAVSKvI9/Qrilfcu/3PWNVfI9pGjlQC3qhCfX/bCq5LfupVkHgK8b53pQPR9F8F8br31BmHZUxLToXLhU98Nc7sb5mf63sORMk7CteKZVoClVJVUTPlaJtTELv70c7H16iEW5F6XE/3VRx8pO/r0qhw9zrz2444WMwS5RuT77rffF8/SpTEHQOtGOkB+7P6UOo45C8VEtn/4iQJ1WhVS5v2VN6QIePzpSDPTy0cfyqwSmc9K0CHMt+Ie4rzfMER2AX3P++2P0QvYwM/vBc689YRALEZV+l/b93Cc5Nmk4gIlG6FSid3KHdrZpHW7BpCXGpqoBiFeQ4ydPGPSZjQ9Eh9EXElURBePXmFRQ32ti2a90KByb4bG4h87NwXiRrs++RyVpeBT/H97Vx8bx1HF357v7HPOTnzYjg1xmqRV1VCqppSigEKEBKFE/FE+BEHlS0ARpCkigBDiQyUCJRGUBkhBLZAKRapCP6IEolREoaIqohKUhDRGVZtQmqQ0cerG7jm2786+r+X35u7svcvd7tzH7tb2G2l1Z+/se29+szdv3syb9xxGUq4f5+Asa3bMLMsGsafahvCdaQzIdRckEUnccSdF4AFvDTxjR49lMe//LY2Nvk5v2rENcVHynvOhSISi27dR/IbrKY1jYqkHkIGL915Zn8NsC8Ihr339OlisXRT52G0qk1nNBc/wsbVF37gLAFbPj12JrrImkYQlC0/teov5h8MUQ1a67l//ciYNZ35pHSFNf7KdYl/cTAHsqRfttQww6Ya1aj1DxtZ8CuFujQsX7MUoEJmAF3krAgMxH76CK66iti1YEocDntNZ7aoMcLQs/r1tFH7yCAUtMfCdcDFhjccQdS2KIEEthYA4QQSC6caxxYl1Byl96jSlcdKiOMky0e+tt26gEALoBDFxC8OvoK5+dxLM5fu8rTIIpzaNKG0ZuHge+tmD90tQDJf6RJS4S8Ay2VXhqwfPTp2ZxNdoNTb8I9g9OkybO6PU7qS5XJTVa9Kd239ArZblVsYhjmxZnElMJ1e4UpyIqT798ivUviIf6IQH9OhdX6bhPcjoFa/PKlN0sOc7ioAgPXDe4jPMOoUHtez+AzSCfMo9P92pJidKwbAygze30j/IE17izcZKu8QzOc9JtQ14TB5FngikrrUrSpGBRtenNl3pEKYhOELJULIRJY7nObZ98rnnKYIjY9ZpSLivl5YeeoyGV9+EiUZemA54pFuVFrczwVHUhoac1xIKxM0/HaUpzhoH5V2cDCzGCYdLezBnjl3WaHXlKjlsiYzeuZW679tFQc0kK6rf9z5Eo5jAdd+7U8U6KE5iuuDsqJrNk5aZwn1e+EN9nUVMORHiiv8Z+QA4A1rdLXH7QZNeSk/TgfExHUbT71h9w6NPn3pOp67UqQMB2ROvAzTdR6DAOaUTDrLalyx+6uf10vg5kZob92GBtGFJ1VrSGEDTe/Zqy68GODihJR55rOQZtoJbkY+74YLgImNsOevvkCsrMAfL9PV7fk7JF07PPlk4H2zACjfYSi9eFRR4GsezEsdPUGzXbkp+9ZtQSloDJZqbP4Ncy8UYae1oOoDJCjq++Ws0CYu6lB5WCaDUwt/6OpYlgmQia9iijRtKjhOmkAY0g7jhtVjQBjBJcBwBS2FsQ0gL2khRMiBNaAzJaDSTeSh2/FwWR91iP95FU9YUojP9bulzfgeK/7eo6TQiycW537ftoCmkrzUsDpaNtMmtZ/8HnwhN0zoOBV772U+3BJ+HdEWJu9ypA9S/EyxszaksBoGHxmMuS+IWeahTyG9iz9dEkI+Zy+bYSfj2T1AQS8hUqJ/DJx/JCuidNy1pSJaXKq188X0RLCDjrdfNDpG8b1dWh81WOwXG9zJIupI8+e8Kz9oPX1kssU58+gs08v0fErfNRExzdS687FIyWGQbRyKMGJbyJz/5Wco88CCb45U7rRzrsraVt7Xq39xHZTxUgBmWd4Ym13F+dzhj2xQmYTke3C3ycNCXJbCSQzh+Ftr0cQpGsShluT8FjI1k0plBWY0U+p15FeU0IHPHRz9MhGxyMxYsv5cl2Di3RVnDCL3KKzzWdjAdu6UO5pmFP8Y49/t37kYTq/d78T3IQWbmcZknAF/aQvFNn6Psvoe1AuXUDFiTH9g7oTVeZVZ39d3XZNZCrgyBN+6KzTzpqmvCq258aersU2hO1SV1buraRRH6Vc8yWtYyN3c48lm3Zoty8qmihDjpRfn5aa5b78tYyaeAY6MXixqYy/abdfmVt4tpBlh6DcXGdYt8Wz//GQrCiam8TONoW4aXzWugy85wubrRKpWgvC2VsLJiafezzD/LNa7sSbYWeNp0Rb/XgGU579r7nbO8ObpbKDYV+72GdzTf76ZaHQiVpall+mlsP6SwLcB1VNwDzffJDn+v7p3CUvpXRi7Qf6ennLZw4u+/Ze27/3L8GcfVSK9kn4986h035yMWbrbp7yA+m2uxAif2hH60fyW9J9yuY/i4KavQFgQEAUGgKgL7YIV/e+Sizjj1Goj0CZTuIiDL6e7iW6TOh1Bt12B5Ir4/OWa7ZOeNqMJFEBAEBIHqCBxIjOsocI4GfE5wdB8BUeLuY0wDtPwQ2NhGb2MxTiH8Z5NWST1olbAQBASBhYYAb+WcTtmfmChgknlb9/J7Fho+frRXlLgHqPeu7B8Gm9l4nlV4XoaH+oLyUvcAe2EhCAgCzUPgP9gPT+tFaUtfd/P1vI0oxWUERIm7DDCTf/bcsZcxgeUIJLbuK+dhiR/Xm+V6ILWwEAQEAUGgFIGjiC7JUSadCuJP/u3gE0eHnOrJ/cYRECXeOIZaFFoo8E9UrLqknk9TSPT7yTFZUddCVCoJAoKAlwjAF50OTiLNrLMlnuzt7OTUclI8QECUuAcgM4sP3rTxGD5s40ryAZwXxRL3qEeEjSAgCNSCQBbmxRm98Sm1ccMHdtdCW+rWj4AcMasfu5qfBNi/gLG91e5BDkm5pauHvtt15ZnimhnKA4KAICAINIhAMQLEHaMX6QhCrTodaYdleBgL7rc1yFYe10RALHFNoJpRLUKdT4CObZYKDvc4lE1TuhkMhYYgIAgIAg0jYFAC49IlJHpxUuBglR5o6d7XMEshoI2AKHFtqBqvuP7m954BFVtnD/6RHJwYp1ehyKUIAoKAIOA/Aib9C9HZjie1kgpNR/uWnPBf5oUjgShxD/v6yInHX8CS+j+cWZp0MlVbWklnmlJDEBAEBIH6EHg2o3U2nIlfHhw682J9XOSpehAQJV4Pag08s5SWcvol24wP7P15eKL+lIoNiCePCgKCgCBQggDHdX8cq4MaJdMbaPuNRj2p0kQERIk3EUwdUtesvPZ51HNMATRt5ojjFkoRBAQBQcBPBBBHEmORxm44Uepd69bLfrjHnSXe6R4DXmB3BJ8b7VhzQpQ/DlxNbw+F/ZFQuAoCgoAgAAQOJSdo66tIzYrvDmfEz6PKcgHNWwTmZt5LbzFygxsr8VtxVV0JYS/124fOUQtzl6mWG33QFJotOTPRZtIYplqvtRINt1JgtIWMCfTbNLoNiyk4oGOYQdgxQQyCIf7Exd3agrgA3LO8WokMmWYIldth8XTgM5LBBdfGxdiJ7MoGDH9ncsWR2yjL58oI5u9xQ1SG1OJV/F8h86dqI9ofNA1DvdJS5g4CKUShyjoHeOGFw5Nzp1XzR1JR4j705Zredz49eOkYR2/rsGOfzHF4BdHgPnSRHkvTzGIWloCijSXJGAmpi0bwoxqDIk+i76CLlRZn5d2ag6JmJc4KPM8gwIqP67CRw4ouhDphKHIo8Vw0Rbm+NJlvSeeoB8rP9l3RE1izlmmyTBmehOQnIrNrqWVvo1Le+ftG8Tu3RSnzwnOFSYqatPBEppWxIMMAVFLmAgIchEqjZN+3Zu29Tw4+o1FVqjQTAVHizURTk1b38qUxuqQSotgOzByG1SHcuiZHqeYSAi3QcD2wmHvQT6vAY8Kg3BiU9xiUGp/HYWXIBbreZMXNKy+sB7ln2UpnRcl1+F4Yg2UEN9rx2Y4qsL7NCP6/RFFwtoSa2UQeF2ocG7QG+lkZvW1PM7ERWpURiEOB/1XA8R4BMfO8x7zI8Uf4crd/7IWzRwiwdrP+zvhv9hXilRi+2NLtwrXYI3mEjSDgBgKcbvkjbhAWmvYIiHe6f28IJwiQw+D+4e8V5/KJMv+NJE8UxbUM11WiwL3qCuHjEgLJ3sDi/S7RFrIOCIgl7u8r8grYD/grgnAXBAQBQaAhBHhrEFtKUvxAQCxxP1Cf5cnR25yT8/oro3AXBAQBQcAOgbMCj38IiBL3D3vqp/7fgX3VHOM+iiasBQFBQBDQQWD6lhU3im+PDlIu1REl7hKwOmTbejsuoh4vRdXo2qtDXeoIAoKAIOA6AoklA29+ynUuwqAqArIn7v/LwWEKP4SLj5vVeKzHf+FFAkFAEFiwCLBjLkdpu3bBIvAGaPj/AV8eTB5YBsljAAAAAElFTkSuQmCC" alt="Logo SMPN 14">
    <div class="divider-v"></div>
    <div class="header-text">
      <h1>KORAN PALASTA</h1>
      <p>SKOR &amp; PENGHARGAAN &nbsp;·&nbsp; SMP Negeri 14 Kota Tangerang</p>
    </div>
    <div class="header-badge" id="tgl-header"></div>
  </div>
  <div class="tabs">
    <div class="tabs-inner">
      <button class="tab-btn active"  onclick="showTab('catat',this)">✍️ Catat Pelanggaran</button>
      <button class="tab-btn" onclick="showTab('daftar',this)">📋 Daftar Siswa</button>
      <button class="tab-btn" onclick="showTab('riwayat',this)">📜 Riwayat</button>
      <button class="tab-btn" onclick="showTab('impexp',this)">📂 Import / Export</button>
      <button class="tab-btn" onclick="showTab('referensi',this)">📘 Tabel Poin</button>
      <button class="tab-btn" onclick="showTab('sanksi',this)">⚖️ Sanksi</button>
    </div>
  </div>
</header>

<main>

<!-- TAB: CATAT -->
<div id="tab-catat" class="section active">
  <div id="status-bar-catat" class="status-bar"></div>
  <div class="card">
    <div class="card-title">Form Pencatatan Pelanggaran</div>
    <div class="form-grid">
      <div>
        <label>Kelas *</label>
        <input id="f-kelas" type="text" placeholder="Contoh: 7A / 8B / 9C" oninput="autoFillKelas()">
      </div>
      <div>
        <label>Nama Siswa *</label>
        <input id="f-nama" type="text" placeholder="Ketik atau pilih dari daftar" list="dl-siswa" oninput="previewSiswa()">
        <datalist id="dl-siswa"></datalist>
      </div>
      <div class="full">
        <label>Jenis Pelanggaran *</label>
        <select id="f-pelanggaran" onchange="onPelanggaranChange()">
          <option value="">-- Pilih jenis pelanggaran --</option>
        </select>
      </div>
      <div>
        <label>Poin Pelanggaran</label>
        <input id="f-poin" type="number" min="1" placeholder="Otomatis / isi manual">
      </div>
      <div>
        <label>Tanggal</label>
        <input id="f-tanggal" type="date">
      </div>
      <div class="full">
        <label>Keterangan Tambahan</label>
        <textarea id="f-ket" rows="2" placeholder="Opsional – detail kejadian"></textarea>
      </div>
      <div class="full" style="display:flex;gap:10px;flex-wrap:wrap;margin-top:4px;">
        <button class="btn btn-primary" onclick="simpanPelanggaran()">💾 Simpan Pelanggaran</button>
        <button class="btn btn-danger"  onclick="resetForm()">🗑️ Reset</button>
      </div>
    </div>
  </div>
  <div class="card" id="preview-card" style="display:none;">
    <div class="card-title">Status Siswa Setelah Pencatatan</div>
    <div id="preview-content"></div>
  </div>
</div>

<!-- TAB: DAFTAR SISWA -->
<div id="tab-daftar" class="section">
  <div class="card" style="padding:14px 20px;">
    <div class="search-row">
      <input type="text" id="search-siswa" placeholder="🔍 Cari nama siswa..." oninput="renderDaftar()">
      <select id="filter-kelas" onchange="renderDaftar()"><option value="">Semua Kelas</option></select>
      <select id="filter-status" onchange="renderDaftar()">
        <option value="">Semua Status</option>
        <option value="aman">Aman (0–49)</option>
        <option value="ringan">Ringan (50–89)</option>
        <option value="sedang">Sedang (90–149)</option>
        <option value="berat">Berat (150–289)</option>
        <option value="kritis">Kritis (290+)</option>
      </select>
      <button class="btn btn-warning btn-sm" onclick="exportExcelDaftar()">📊 Export Daftar</button>
    </div>
  </div>
  <div id="daftar-list"></div>
</div>

<!-- TAB: RIWAYAT -->
<div id="tab-riwayat" class="section">
  <div class="card" style="padding:14px 20px;">
    <div class="search-row">
      <input type="text" id="search-riwayat" placeholder="🔍 Cari nama / pelanggaran..." oninput="renderRiwayat()">
      <button class="btn btn-warning btn-sm" onclick="exportExcelRiwayat()">📊 Export Riwayat</button>
      <button class="btn btn-danger btn-sm" onclick="hapusSemuaRiwayat()">🗑️ Hapus Semua</button>
    </div>
  </div>
  <div class="card"><div id="riwayat-list"></div></div>
</div>

<!-- TAB: IMPORT / EXPORT -->
<div id="tab-impexp" class="section">

  <div class="card">
    <div class="card-title">📤 Import Data Siswa dari CSV / Excel</div>
    <div class="upload-area" onclick="document.getElementById('file-input-csv').click()" id="upload-area"
         ondragover="dragOver(event)" ondragleave="dragLeave(event)" ondrop="dropFile(event)">
      <div class="icon">📂</div>
      <p><strong>Klik untuk pilih file</strong> atau seret file ke sini</p>
      <p style="margin-top:6px;font-size:11.5px;">Format: <strong>.CSV</strong> atau <strong>.TSV</strong> — kolom wajib: <code>nama</code>, <code>kelas</code></p>
      <p style="margin-top:4px;font-size:11px;color:#9CA3AF;">Kolom opsional: <code>poin</code>, <code>pelanggaran</code>, <code>tanggal</code>, <code>keterangan</code></p>
    </div>
    <input type="file" id="file-input-csv" accept=".csv,.tsv,.txt" onchange="handleFileUpload(event)">

    <div id="preview-import">
      <div style="display:flex;align-items:center;gap:10px;margin-bottom:8px;">
        <span id="preview-info" style="font-size:13px;font-weight:600;color:var(--merah-tua);"></span>
        <button class="btn btn-success btn-sm" onclick="konfirmasiImport()">✅ Konfirmasi Import</button>
        <button class="btn btn-danger btn-sm" onclick="batalImport()">✕ Batal</button>
      </div>
      <div class="preview-table-wrap">
        <table id="preview-table">
          <thead><tr id="preview-head"></tr></thead>
          <tbody id="preview-body"></tbody>
        </table>
      </div>
    </div>

    <div style="margin-top:18px;">
      <div class="card-title" style="margin-bottom:10px;">📋 Format CSV yang Benar</div>
      <div style="background:#F8F8F8;border-radius:8px;padding:14px;font-size:12.5px;font-family:monospace;color:#374151;line-height:1.8;border:1px solid #E5E7EB;">
        nama,kelas,poin,pelanggaran,tanggal,keterangan<br>
        Ahmad Fauzi,7A,10,Tidak mengerjakan PR,2026-06-01,Sudah diperingatkan<br>
        Siti Rahayu,8B,5,Terlambat masuk sekolah,2026-06-02,<br>
        Budi Santoso,9C,30,Bolos tanpa keterangan,,<br>
      </div>
      <p style="font-size:11.5px;color:var(--abu);margin-top:8px;">💡 Tip: Buat di Excel → Save As → CSV (Comma delimited). Kolom <code>poin</code>, <code>tanggal</code>, <code>keterangan</code> boleh dikosongkan.</p>
      <button class="btn btn-warning btn-sm" style="margin-top:10px;" onclick="downloadTemplate()">⬇️ Download Template CSV</button>
    </div>
  </div>

  <div class="card">
    <div class="card-title">📥 Unduh Data Pelanggaran</div>
    <div class="export-grid">
      <div class="export-card" onclick="exportExcelRiwayat()">
        <div class="icon">📊</div>
        <h4>Riwayat Pelanggaran (CSV)</h4>
        <p>Semua catatan pelanggaran dengan detail nama, kelas, poin, tanggal</p>
        <button class="btn btn-success btn-sm" style="margin-top:12px;">⬇️ Unduh CSV</button>
      </div>
      <div class="export-card" onclick="exportExcelDaftar()">
        <div class="icon">📋</div>
        <h4>Rekap Per Siswa (CSV)</h4>
        <p>Total poin per siswa, jumlah pelanggaran, dan status sanksi</p>
        <button class="btn btn-success btn-sm" style="margin-top:12px;">⬇️ Unduh CSV</button>
      </div>
      <div class="export-card" onclick="exportHTML()">
        <div class="icon">🖨️</div>
        <h4>Cetak Laporan (Print)</h4>
        <p>Buka tampilan cetak untuk dicetak atau disimpan sebagai PDF</p>
        <button class="btn btn-primary btn-sm" style="margin-top:12px;">🖨️ Cetak</button>
      </div>
      <div class="export-card" onclick="backupData()">
        <div class="icon">💾</div>
        <h4>Backup Data (JSON)</h4>
        <p>Simpan seluruh data untuk backup atau dipindah ke komputer lain</p>
        <button class="btn btn-warning btn-sm" style="margin-top:12px;">⬇️ Backup JSON</button>
      </div>
    </div>
    <div style="margin-top:16px;padding-top:16px;border-top:1px solid #F0F0F0;">
      <div class="card-title" style="margin-bottom:10px;">♻️ Pulihkan Data dari Backup</div>
      <div style="display:flex;gap:10px;align-items:center;flex-wrap:wrap;">
        <input type="file" id="restore-input" accept=".json" onchange="restoreData(event)" style="flex:1;min-width:180px;">
        <span style="font-size:12px;color:var(--abu);">Upload file backup .json untuk memulihkan data</span>
      </div>
    </div>
  </div>
</div>

<!-- TAB: REFERENSI -->
<div id="tab-referensi" class="section">
  <div class="card">
    <div class="card-title">Tabel Kredit Poin Pelanggaran Tata Tertib</div>
    <div class="search-row">
      <input type="text" id="search-tabel" placeholder="🔍 Cari jenis pelanggaran..." oninput="renderTabelRef()">
      <select id="filter-kategori" onchange="renderTabelRef()">
        <option value="">Semua Kategori</option>
        <option value="ringan">Ringan</option>
        <option value="sedang">Sedang</option>
        <option value="berat">Berat</option>
      </select>
    </div>
    <div class="tbl-wrap">
      <table>
        <thead><tr><th style="width:40px">No</th><th>Jenis Pelanggaran</th><th style="width:100px">Kategori</th><th style="width:70px;text-align:center">Poin</th></tr></thead>
        <tbody id="tabel-ref-body"></tbody>
      </table>
    </div>
  </div>
</div>

<!-- TAB: SANKSI -->
<div id="tab-sanksi" class="section">
  <div class="card">
    <div class="card-title">Tindak Lanjut Akumulasi Poin Pelanggaran</div>
    <div class="sanksi-panel">
      <div class="sanksi-tier ringan">
        <h4>🟡 RINGAN — Poin 1–49</h4>
        <ul>
          <li>Teguran lisan oleh guru / walikelas / BK</li>
          <li>Membersihkan lingkungan sekolah dan masjid</li>
          <li>Tilawah 1 juz</li>
          <li>1–2 teguran bagi yang kesiangan</li>
        </ul>
      </div>
      <div class="sanksi-tier sedang">
        <h4>🟠 SEDANG — Poin 50–89</h4>
        <ul>
          <li>Pemanggilan oleh BK</li>
          <li>Menyumbang pot beserta bunganya</li>
          <li>Tilawah 2 juz</li>
          <li>Pemanggilan orangtua (≥3× kesiangan)</li>
          <li>Dipulangkan jika 4–5× kesiangan</li>
        </ul>
      </div>
      <div class="sanksi-tier berat">
        <h4>🔴 BERAT (90–149) — SP Awal</h4>
        <ul>
          <li>Pemanggilan & teguran lisan siswa + orangtua</li>
          <li>Tilawah 3 juz</li>
        </ul>
        <h4 class="sub">🔴 BERAT (150–189) — SP 1</h4>
        <ul>
          <li>Surat Peringatan ke-1</li>
          <li>Skorsing 3 (tiga) hari</li>
          <li>Hafal surat Al-Munafiqun</li>
        </ul>
        <h4 class="sub">🔴 BERAT (190–289) — SP 2</h4>
        <ul>
          <li>Surat Peringatan ke-2</li>
          <li>Skorsing 6 (enam) hari</li>
          <li>Tidak bisa ikut PAS & PAT</li>
          <li>Hafal Q.S. Al-Baqarah ayat 1–20</li>
        </ul>
      </div>
      <div class="sanksi-tier kritis">
        <h4>⛔ KRITIS — Poin 290–300+</h4>
        <ul>
          <li>SP 3 / Dikembalikan ke orangtua</li>
          <li>Berdasarkan musyawarah sekolah</li>
          <li>Prosedur persidangan pihak terkait</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-title">Kalkulator Poin & Sanksi</div>
    <div style="display:flex;gap:12px;align-items:flex-end;flex-wrap:wrap;">
      <div style="flex:1;min-width:180px;">
        <label>Masukkan Total Poin Siswa</label>
        <input type="number" id="kalk-poin" min="0" placeholder="Contoh: 75" oninput="kalkulasiSanksi()">
      </div>
    </div>
    <div id="kalk-result" style="margin-top:14px;"></div>
  </div>
</div>

</main>

<!-- MODAL DETAIL SISWA -->
<div class="modal-overlay" id="modal-detail">
  <div class="modal">
    <div id="modal-content"></div>
    <div style="margin-top:16px;display:flex;gap:8px;flex-wrap:wrap;">
      <button class="btn btn-danger btn-sm" onclick="hapusSiswa()">🗑️ Hapus Data Siswa</button>
      <button class="btn btn-warning btn-sm" onclick="exportSiswa()">📊 Export Siswa Ini</button>
      <button class="btn btn-primary btn-sm" style="margin-left:auto;" onclick="tutupModal()">Tutup</button>
    </div>
  </div>
</div>

<div id="toast"></div>

<script>
// ============================================================
//  DATA PELANGGARAN
// ============================================================
const PELANGGARAN = [
  { id:1,  nama:"Terlambat masuk sekolah (1–2×)",                  kategori:"ringan", poin:5   },
  { id:2,  nama:"Tidak memakai seragam lengkap / atribut",          kategori:"ringan", poin:5   },
  { id:3,  nama:"Rambut tidak rapi (laki-laki terlalu panjang)",    kategori:"ringan", poin:5   },
  { id:4,  nama:"Tidak membawa buku/alat pelajaran",                kategori:"ringan", poin:5   },
  { id:5,  nama:"Membuang sampah sembarangan",                      kategori:"ringan", poin:5   },
  { id:6,  nama:"Ribut di kelas / mengganggu pelajaran",            kategori:"ringan", poin:5   },
  { id:7,  nama:"Tidak mengerjakan PR / tugas sekolah",             kategori:"ringan", poin:10  },
  { id:8,  nama:"Makan/minum di dalam kelas saat KBM",              kategori:"ringan", poin:5   },
  { id:9,  nama:"Tidak membawa kartu pelajar",                      kategori:"ringan", poin:5   },
  { id:10, nama:"Memakai perhiasan berlebihan (perempuan)",          kategori:"ringan", poin:5   },
  { id:11, nama:"Kuku panjang / diwarnai",                          kategori:"ringan", poin:5   },
  { id:12, nama:"Tidak rapi saat upacara bendera",                  kategori:"ringan", poin:10  },
  { id:13, nama:"Bermain HP saat KBM tanpa izin guru",              kategori:"ringan", poin:10  },
  { id:14, nama:"Tidak shalat berjamaah tanpa alasan jelas",        kategori:"ringan", poin:10  },
  { id:15, nama:"Terlambat masuk sekolah (3–5×)",                   kategori:"ringan", poin:15  },
  { id:16, nama:"Berpakaian tidak sesuai hari yang ditentukan",     kategori:"ringan", poin:5   },
  { id:17, nama:"Tidak membawa buku saku siswa",                    kategori:"ringan", poin:5   },
  { id:18, nama:"Berlari-lari di dalam kelas/koridor",              kategori:"ringan", poin:5   },
  { id:19, nama:"Terlambat masuk sekolah (6–10×)",                  kategori:"sedang", poin:25  },
  { id:20, nama:"Keluar kelas tanpa izin",                          kategori:"sedang", poin:15  },
  { id:21, nama:"Meninggalkan sekolah tanpa izin (bolos)",          kategori:"sedang", poin:30  },
  { id:22, nama:"Tidak mengikuti upacara bendera",                  kategori:"sedang", poin:20  },
  { id:23, nama:"Membawa dan menggunakan HP saat ulangan",           kategori:"sedang", poin:25  },
  { id:24, nama:"Bertengkar/berkelahi verbal di lingkungan sekolah", kategori:"sedang", poin:30  },
  { id:25, nama:"Membawa bacaan / gambar tidak layak",              kategori:"sedang", poin:25  },
  { id:26, nama:"Berbohong/mencontek saat ulangan",                 kategori:"sedang", poin:25  },
  { id:27, nama:"Merusak fasilitas sekolah (ringan)",               kategori:"sedang", poin:30  },
  { id:28, nama:"Mengintimidasi / mengejek teman",                  kategori:"sedang", poin:30  },
  { id:29, nama:"Tidak masuk sekolah tanpa keterangan 1–3 hari",   kategori:"sedang", poin:20  },
  { id:30, nama:"Merokok di lingkungan sekolah",                    kategori:"sedang", poin:50  },
  { id:31, nama:"Memalsukan tanda tangan / surat izin",             kategori:"sedang", poin:40  },
  { id:32, nama:"Berpacaran / berperilaku tidak sopan",             kategori:"sedang", poin:30  },
  { id:33, nama:"Perkelahian fisik di lingkungan sekolah",          kategori:"berat",  poin:75  },
  { id:34, nama:"Membawa senjata tajam / berbahaya",                kategori:"berat",  poin:100 },
  { id:35, nama:"Terlibat narkoba / minuman keras",                 kategori:"berat",  poin:200 },
  { id:36, nama:"Mencuri barang milik orang lain",                  kategori:"berat",  poin:100 },
  { id:37, nama:"Merusak fasilitas sekolah secara sengaja (berat)", kategori:"berat",  poin:75  },
  { id:38, nama:"Tidak masuk sekolah tanpa keterangan lebih dari 5 hari", kategori:"berat", poin:60 },
  { id:39, nama:"Melakukan pelecehan seksual",                      kategori:"berat",  poin:200 },
  { id:40, nama:"Berjudi di lingkungan sekolah",                    kategori:"berat",  poin:100 },
  { id:41, nama:"Memeras / bullying fisik",                         kategori:"berat",  poin:100 },
  { id:42, nama:"Menyebarkan konten asusila melalui media sosial",  kategori:"berat",  poin:150 },
  { id:43, nama:"Membawa / menggunakan petasan",                    kategori:"berat",  poin:75  },
  { id:44, nama:"Melakukan tindak kriminal",                        kategori:"berat",  poin:200 },
  { id:45, nama:"Perkelahian di luar sekolah (melibatkan nama sekolah)", kategori:"berat", poin:100 },
];

// ============================================================
//  STATE
// ============================================================
let riwayat = JSON.parse(localStorage.getItem('rw_smpn14') || '[]');
let selectedSiswaId = null;
let importData = [];

// ============================================================
//  INIT
// ============================================================
window.onload = () => {
  populateSelect();
  renderStatusBar();
  renderTabelRef();
  setDefaultDate();
  updateDatalist();
  document.getElementById('tgl-header').textContent = new Date().toLocaleDateString('id-ID',{weekday:'long',year:'numeric',month:'long',day:'numeric'});
};

function setDefaultDate() {
  document.getElementById('f-tanggal').value = new Date().toISOString().split('T')[0];
}

function populateSelect() {
  const sel = document.getElementById('f-pelanggaran');
  const groups = { ringan:'🟡 RINGAN (1–49 poin)', sedang:'🟠 SEDANG (50–89 poin)', berat:'🔴 BERAT (90–300 poin)' };
  for (const [kat, label] of Object.entries(groups)) {
    const og = document.createElement('optgroup');
    og.label = label;
    PELANGGARAN.filter(p => p.kategori === kat).forEach(p => {
      const o = document.createElement('option');
      o.value = p.id;
      o.textContent = `${p.nama} [${p.poin} poin]`;
      og.appendChild(o);
    });
    sel.appendChild(og);
  }
}

function updateDatalist() {
  const dl = document.getElementById('dl-siswa');
  dl.innerHTML = '';
  getSiswaList().forEach(s => {
    const o = document.createElement('option'); o.value = s.nama; dl.appendChild(o);
  });
}

// ============================================================
//  HELPERS
// ============================================================
function getSiswaList() {
  const map = {};
  riwayat.forEach(r => {
    const key = r.nama.trim().toLowerCase() + '|||' + r.kelas.trim().toLowerCase();
    if (!map[key]) map[key] = { id:key, nama:r.nama, kelas:r.kelas, totalPoin:0, count:0 };
    map[key].totalPoin += r.poin;
    map[key].count++;
  });
  return Object.values(map).sort((a,b) => b.totalPoin - a.totalPoin);
}

function getSanksiInfo(p) {
  if (p >= 290) return { label:'KRITIS – Dikembalikan ke Orangtua', cls:'sanksi-kritis', icon:'⛔' };
  if (p >= 190) return { label:'SP 2 – Skorsing 6 Hari', cls:'sanksi-berat', icon:'🔴' };
  if (p >= 150) return { label:'SP 1 – Skorsing 3 Hari', cls:'sanksi-berat', icon:'🔴' };
  if (p >= 90)  return { label:'Peringatan & Panggil Orangtua', cls:'sanksi-berat', icon:'🔴' };
  if (p >= 50)  return { label:'Pemanggilan BK + Orangtua', cls:'sanksi-sedang', icon:'🟠' };
  if (p >= 1)   return { label:'Teguran & Tugas Kebersihan', cls:'sanksi-ringan', icon:'🟡' };
  return { label:'Tidak Ada Pelanggaran', cls:'sanksi-aman', icon:'✅' };
}

function getKatBadge(k) {
  const m = { ringan:'badge-ringan', sedang:'badge-sedang', berat:'badge-berat' };
  const l = { ringan:'Ringan', sedang:'Sedang', berat:'Berat' };
  return `<span class="badge ${m[k]||'badge-sedang'}">${l[k]||k}</span>`;
}

function poinColor(p) {
  if (p >= 290) return '#7F1D1D';
  if (p >= 90)  return '#B91C1C';
  if (p >= 50)  return '#D97706';
  return '#059669';
}

function escHtml(s) {
  return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');
}

function formatTgl(d) {
  if (!d) return '–';
  const [y,m,dd] = d.split('-');
  const b = ['Jan','Feb','Mar','Apr','Mei','Jun','Jul','Agt','Sep','Okt','Nov','Des'];
  return `${parseInt(dd)} ${b[parseInt(m)-1]} ${y}`;
}

function simpanStorage() { localStorage.setItem('rw_smpn14', JSON.stringify(riwayat)); }
function showToast(msg, dur=3000) {
  const t = document.getElementById('toast'); t.textContent = msg; t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), dur);
}

// ============================================================
//  FORM PENCATATAN
// ============================================================
function autoFillKelas() {
  const nama = document.getElementById('f-nama').value.trim().toLowerCase();
  if (!nama) return;
  const siswa = getSiswaList().find(s => s.nama.toLowerCase() === nama);
  if (siswa && !document.getElementById('f-kelas').value) {
    document.getElementById('f-kelas').value = siswa.kelas;
  }
  previewSiswa();
}

function onPelanggaranChange() {
  const id = parseInt(document.getElementById('f-pelanggaran').value);
  const p = PELANGGARAN.find(x => x.id === id);
  if (p) document.getElementById('f-poin').value = p.poin;
  previewSiswa();
}

function previewSiswa() {
  const nama = document.getElementById('f-nama').value.trim();
  if (!nama) { document.getElementById('preview-card').style.display='none'; return; }
  const siswa = getSiswaList().find(s => s.nama.toLowerCase() === nama.toLowerCase());
  if (siswa && !document.getElementById('f-kelas').value) {
    document.getElementById('f-kelas').value = siswa.kelas;
  }
  const poinTambah = parseInt(document.getElementById('f-poin').value) || 0;
  const poinLama = siswa ? siswa.totalPoin : 0;
  const poinBaru = poinLama + poinTambah;
  const sanksi = getSanksiInfo(poinBaru);
  const pct = Math.min(100, (poinBaru / 300) * 100);
  const barC = poinColor(poinBaru);
  const kls = document.getElementById('f-kelas').value || (siswa ? siswa.kelas : '–');

  document.getElementById('preview-card').style.display = 'block';
  document.getElementById('preview-content').innerHTML = `
    <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap;">
      <div style="flex:1;min-width:200px;">
        <div style="font-weight:700;font-size:15px;">${escHtml(nama)}</div>
        <div style="font-size:12px;color:var(--abu);margin-bottom:8px;">Kelas ${escHtml(kls)} &nbsp;·&nbsp; Poin lama: <b>${poinLama}</b> → setelah: <b>${poinBaru}</b></div>
        <div class="progress-wrap"><div class="progress-bar" style="width:${pct}%;background:${barC};"></div></div>
        <div style="font-size:11px;color:var(--abu);margin-top:4px;">${poinBaru} / 300 poin</div>
      </div>
      <div style="text-align:center;">
        <div style="font-size:32px;font-weight:900;color:${barC};">${poinBaru}</div>
        <div style="font-size:11px;color:var(--abu);">Total Poin</div>
        <div class="sanksi-badge ${sanksi.cls}" style="margin-top:8px;">${sanksi.icon} ${sanksi.label}</div>
      </div>
    </div>
  `;
}

function simpanPelanggaran() {
  const nama  = document.getElementById('f-nama').value.trim();
  const kelas = document.getElementById('f-kelas').value.trim();
  const pelId = parseInt(document.getElementById('f-pelanggaran').value);
  const poin  = parseInt(document.getElementById('f-poin').value);
  const tgl   = document.getElementById('f-tanggal').value;
  const ket   = document.getElementById('f-ket').value.trim();
  if (!nama)        return showToast('⚠️ Nama siswa wajib diisi!');
  if (!kelas)       return showToast('⚠️ Kelas wajib diisi!');
  if (!poin || poin < 1) return showToast('⚠️ Poin tidak valid!');
  const pel   = PELANGGARAN.find(p => p.id === pelId);
  const namaP = pel ? pel.nama : 'Pelanggaran lainnya';
  const katP  = pel ? pel.kategori : 'sedang';
  riwayat.unshift({ id:Date.now(), nama, kelas, namaP, poin, kategori:katP, tanggal:tgl||new Date().toISOString().split('T')[0], keterangan:ket });
  simpanStorage(); updateDatalist(); renderStatusBar(); previewSiswa();
  showToast(`✅ Disimpan: "${namaP}" — ${poin} poin`);
}

function resetForm() {
  ['f-nama','f-kelas','f-poin','f-ket'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('f-pelanggaran').value = '';
  setDefaultDate();
  document.getElementById('preview-card').style.display = 'none';
}

// ============================================================
//  STATUS BAR
// ============================================================
function renderStatusBar() {
  const sl = getSiswaList();
  document.getElementById('status-bar-catat').innerHTML = `
    <div class="status-item"><div class="status-num">${sl.length}</div><div class="status-label">Total Siswa</div></div>
    <div class="status-item kuning"><div class="status-num kuning">${riwayat.length}</div><div class="status-label">Total Catatan</div></div>
    <div class="status-item merah"><div class="status-num merah">${sl.filter(s=>s.totalPoin>=90&&s.totalPoin<290).length}</div><div class="status-label">Siswa Berisiko</div></div>
    <div class="status-item merah"><div class="status-num merah">${sl.filter(s=>s.totalPoin>=290).length}</div><div class="status-label">Siswa Kritis (SP)</div></div>
  `;
}

// ============================================================
//  DAFTAR SISWA
// ============================================================
function renderDaftar() {
  const q = document.getElementById('search-siswa').value.toLowerCase();
  const fk = document.getElementById('filter-kelas').value.toLowerCase();
  const fs = document.getElementById('filter-status').value;

  const kelasSet = new Set(riwayat.map(r => r.kelas.trim()));
  const selKls = document.getElementById('filter-kelas');
  const curKls = selKls.value;
  selKls.innerHTML = '<option value="">Semua Kelas</option>';
  [...kelasSet].sort().forEach(k => {
    const o = document.createElement('option'); o.value = k; o.textContent = k;
    if (k.toLowerCase() === curKls.toLowerCase()) o.selected = true;
    selKls.appendChild(o);
  });

  let sl = getSiswaList();
  if (q)  sl = sl.filter(s => s.nama.toLowerCase().includes(q));
  if (fk) sl = sl.filter(s => s.kelas.toLowerCase() === fk);
  if (fs) sl = sl.filter(s => {
    const p = s.totalPoin;
    return fs==='aman'?p<50:fs==='ringan'?p>=50&&p<90:fs==='sedang'?p>=90&&p<150:fs==='berat'?p>=150&&p<290:p>=290;
  });

  const el = document.getElementById('daftar-list');
  if (!sl.length) { el.innerHTML = '<div class="empty-state"><div class="icon">📭</div>Tidak ada data siswa.</div>'; return; }

  el.innerHTML = sl.map(s => {
    const sanksi = getSanksiInfo(s.totalPoin);
    const pct = Math.min(100,(s.totalPoin/300)*100);
    const barC = poinColor(s.totalPoin);
    const init = s.nama.split(' ').slice(0,2).map(w=>w[0]).join('').toUpperCase();
    return `
      <div class="siswa-card" onclick="bukaSiswa(${JSON.stringify(s.id)})">
        <div class="siswa-avatar">${init}</div>
        <div class="siswa-info">
          <div class="siswa-nama">${escHtml(s.nama)}</div>
          <div class="siswa-meta">Kelas ${escHtml(s.kelas)} · ${s.count} pelanggaran</div>
          <div class="progress-wrap" style="margin-top:6px;"><div class="progress-bar" style="width:${pct}%;background:${barC};"></div></div>
          <div style="margin-top:5px;"><span class="sanksi-badge ${sanksi.cls}" style="font-size:11px;">${sanksi.icon} ${sanksi.label}</span></div>
        </div>
        <div class="siswa-poin-total" style="color:${barC}">${s.totalPoin}</div>
      </div>`;
  }).join('');
}

// ============================================================
//  RIWAYAT
// ============================================================
function renderRiwayat() {
  const q = document.getElementById('search-riwayat').value.toLowerCase();
  let list = riwayat;
  if (q) list = list.filter(r => r.nama.toLowerCase().includes(q) || r.namaP.toLowerCase().includes(q));
  const el = document.getElementById('riwayat-list');
  if (!list.length) { el.innerHTML = '<div class="empty-state"><div class="icon">📋</div>Belum ada riwayat.</div>'; return; }
  const icons = { ringan:'🟡', sedang:'🟠', berat:'🔴' };
  const bgcl  = { ringan:'#FFFBEB', sedang:'#FFF7ED', berat:'#FFF1F2' };
  el.innerHTML = list.map(r => `
    <div class="riwayat-item">
      <div class="riwayat-icon" style="background:${bgcl[r.kategori]||'#F9F9F9'}">${icons[r.kategori]||'📌'}</div>
      <div class="riwayat-info">
        <div class="riwayat-nama">${escHtml(r.nama)} <span style="font-size:11.5px;color:var(--abu);font-weight:400">— Kelas ${escHtml(r.kelas)}</span></div>
        <div class="riwayat-detail">${escHtml(r.namaP)}${r.keterangan?' · '+escHtml(r.keterangan):''}</div>
        <div class="riwayat-detail" style="margin-top:2px;">${formatTgl(r.tanggal)} &nbsp; ${getKatBadge(r.kategori)}</div>
      </div>
      <div style="display:flex;flex-direction:column;align-items:flex-end;gap:5px;">
        <div class="riwayat-poin">+${r.poin}</div>
        <button class="btn btn-danger btn-sm" onclick="hapusRiwayat(${r.id},event)">✕</button>
      </div>
    </div>`).join('');
}

function hapusRiwayat(id, e) {
  e.stopPropagation();
  if (!confirm('Hapus catatan ini?')) return;
  riwayat = riwayat.filter(r => r.id !== id);
  simpanStorage(); renderRiwayat(); renderStatusBar();
  showToast('🗑️ Catatan dihapus.');
}

function hapusSemuaRiwayat() {
  if (!confirm('Hapus SEMUA riwayat pelanggaran?')) return;
  riwayat = []; simpanStorage(); renderRiwayat(); renderStatusBar();
  showToast('🗑️ Semua riwayat dihapus.');
}

// ============================================================
//  TABEL REFERENSI
// ============================================================
function renderTabelRef() {
  const q   = document.getElementById('search-tabel').value.toLowerCase();
  const kat = document.getElementById('filter-kategori').value;
  let list  = PELANGGARAN;
  if (q)   list = list.filter(p => p.nama.toLowerCase().includes(q));
  if (kat) list = list.filter(p => p.kategori === kat);
  document.getElementById('tabel-ref-body').innerHTML = list.map((p,i) => `
    <tr><td style="color:var(--abu);font-size:12px;">${i+1}</td><td>${escHtml(p.nama)}</td><td class="td-center">${getKatBadge(p.kategori)}</td><td class="td-poin">${p.poin}</td></tr>
  `).join('') || `<tr><td colspan="4" class="empty-state">Tidak ada data.</td></tr>`;
}

// ============================================================
//  KALKULATOR SANKSI
// ============================================================
function kalkulasiSanksi() {
  const p = parseInt(document.getElementById('kalk-poin').value);
  const el = document.getElementById('kalk-result');
  if (isNaN(p)||p<0) { el.innerHTML=''; return; }
  const sanksi = getSanksiInfo(p);
  const pct = Math.min(100,(p/300)*100);
  const barC = poinColor(p);
  el.innerHTML = `
    <div style="padding:14px;border-radius:10px;background:#F8F9FA;border:1.5px solid #E5E7EB;">
      <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap;">
        <div style="flex:1;">
          <div style="font-size:13px;color:var(--abu);margin-bottom:6px;">Total: <strong>${p} poin</strong></div>
          <div class="progress-wrap"><div class="progress-bar" style="width:${pct}%;background:${barC};"></div></div>
          <div style="font-size:11px;color:var(--abu);margin-top:4px;">${pct.toFixed(1)}% dari batas 300</div>
        </div>
        <span class="sanksi-badge ${sanksi.cls}">${sanksi.icon} ${sanksi.label}</span>
      </div>
    </div>`;
}

// ============================================================
//  MODAL DETAIL SISWA
// ============================================================
function bukaSiswa(id) {
  selectedSiswaId = id;
  const s = getSiswaList().find(x => x.id === id);
  if (!s) return;
  const catatan = riwayat.filter(r => (r.nama.trim().toLowerCase()+'|||'+r.kelas.trim().toLowerCase()) === id);
  const sanksi = getSanksiInfo(s.totalPoin);
  const pct = Math.min(100,(s.totalPoin/300)*100);
  const barC = poinColor(s.totalPoin);
  const init = s.nama.split(' ').slice(0,2).map(w=>w[0]).join('').toUpperCase();
  const icons = { ringan:'🟡', sedang:'🟠', berat:'🔴' };
  document.getElementById('modal-content').innerHTML = `
    <div style="display:flex;align-items:center;gap:14px;margin-bottom:16px;flex-wrap:wrap;">
      <div class="siswa-avatar" style="width:54px;height:54px;font-size:19px;">${init}</div>
      <div style="flex:1;">
        <div style="font-weight:800;font-size:17px;">${escHtml(s.nama)}</div>
        <div style="font-size:12px;color:var(--abu);">Kelas ${escHtml(s.kelas)}</div>
        <div class="sanksi-badge ${sanksi.cls}" style="margin-top:6px;font-size:11.5px;">${sanksi.icon} ${sanksi.label}</div>
      </div>
      <div style="text-align:center;">
        <div style="font-size:34px;font-weight:900;color:${barC};">${s.totalPoin}</div>
        <div style="font-size:11px;color:var(--abu);">Total Poin</div>
      </div>
    </div>
    <div class="progress-wrap" style="margin-bottom:14px;"><div class="progress-bar" style="width:${pct}%;background:${barC};"></div></div>
    <div style="font-size:12.5px;font-weight:700;margin-bottom:8px;color:var(--merah-tua);">Riwayat Pelanggaran (${catatan.length})</div>
    <div style="max-height:260px;overflow-y:auto;">
      ${catatan.map(r=>`
        <div style="display:flex;gap:10px;padding:7px 0;border-bottom:1px solid #F0F0F0;font-size:12.5px;">
          <span>${icons[r.kategori]||'📌'}</span>
          <div style="flex:1;min-width:0;">
            <div style="font-weight:600;">${escHtml(r.namaP)}</div>
            <div style="font-size:11px;color:var(--abu);">${formatTgl(r.tanggal)}${r.keterangan?' · '+escHtml(r.keterangan):''}</div>
          </div>
          <div style="font-weight:800;color:var(--merah);flex-shrink:0;">+${r.poin}</div>
        </div>`).join('')}
    </div>`;
  document.getElementById('modal-detail').classList.add('show');
}

function tutupModal() { document.getElementById('modal-detail').classList.remove('show'); selectedSiswaId=null; }
function hapusSiswa() {
  if (!selectedSiswaId||!confirm('Hapus semua data siswa ini?')) return;
  riwayat = riwayat.filter(r => (r.nama.trim().toLowerCase()+'|||'+r.kelas.trim().toLowerCase()) !== selectedSiswaId);
  simpanStorage(); tutupModal(); renderDaftar(); renderRiwayat(); renderStatusBar(); updateDatalist();
  showToast('🗑️ Data siswa dihapus.');
}
function exportSiswa() {
  if (!selectedSiswaId) return;
  const s = getSiswaList().find(x => x.id === selectedSiswaId);
  const catatan = riwayat.filter(r => (r.nama.trim().toLowerCase()+'|||'+r.kelas.trim().toLowerCase()) === selectedSiswaId);
  const sanksi = getSanksiInfo(s.totalPoin);
  let csv = 'Nama,Kelas,Tanggal,Pelanggaran,Kategori,Poin,Keterangan\n';
  catatan.forEach(r => {
    csv += `"${r.nama}","${r.kelas}","${r.tanggal}","${r.namaP}","${r.kategori}",${r.poin},"${r.keterangan||''}"\n`;
  });
  csv += `\n"TOTAL POIN",,,,,"${s.totalPoin}"\n"STATUS",,,,,,"${sanksi.label}"\n`;
  downloadCSV(csv, `pelanggaran_${s.nama.replace(/\s+/g,'_')}.csv`);
}
document.getElementById('modal-detail').addEventListener('click', function(e) { if(e.target===this) tutupModal(); });

// ============================================================
//  IMPORT CSV
// ============================================================
function dragOver(e)  { e.preventDefault(); document.getElementById('upload-area').style.borderColor='var(--merah)'; }
function dragLeave(e) { document.getElementById('upload-area').style.borderColor=''; }
function dropFile(e)  { e.preventDefault(); dragLeave(e); processFile(e.dataTransfer.files[0]); }
function handleFileUpload(e) { processFile(e.target.files[0]); }

function processFile(file) {
  if (!file) return;
  const ext = file.name.split('.').pop().toLowerCase();
  if (!['csv','tsv','txt'].includes(ext)) return showToast('⚠️ Format file tidak didukung. Gunakan .csv atau .tsv');
  const reader = new FileReader();
  reader.onload = e => parseCSV(e.target.result);
  reader.readAsText(file, 'UTF-8');
}

function parseCSV(text) {
  const lines = text.trim().split(/\r?\n/).filter(l => l.trim());
  if (lines.length < 2) return showToast('⚠️ File CSV kosong atau tidak valid.');
  const sep = lines[0].includes(';') ? ';' : lines[0].includes('\t') ? '\t' : ',';
  const headers = lines[0].split(sep).map(h => h.trim().toLowerCase().replace(/[^a-z]/g,''));
  const namaIdx = headers.findIndex(h => h.includes('nama'));
  const kelasIdx = headers.findIndex(h => h.includes('kelas'));
  if (namaIdx < 0 || kelasIdx < 0) return showToast('⚠️ Kolom "nama" dan "kelas" wajib ada di file CSV.');
  const poinIdx = headers.findIndex(h => h.includes('poin'));
  const pelIdx  = headers.findIndex(h => h.includes('pelanggaran') || h.includes('jenis'));
  const tglIdx  = headers.findIndex(h => h.includes('tanggal') || h.includes('tgl'));
  const ketIdx  = headers.findIndex(h => h.includes('ket'));
  importData = [];
  lines.slice(1).forEach((line, i) => {
    if (!line.trim()) return;
    const cols = parseCsvLine(line, sep);
    const nama  = (cols[namaIdx]||'').trim();
    const kelas = (cols[kelasIdx]||'').trim();
    if (!nama || !kelas) return;
    importData.push({
      nama, kelas,
      poin:     poinIdx >= 0 ? (parseInt(cols[poinIdx])||10) : 10,
      namaP:    pelIdx  >= 0 ? (cols[pelIdx]||'').trim() : 'Data diimport',
      tanggal:  tglIdx  >= 0 ? (cols[tglIdx]||'').trim() : new Date().toISOString().split('T')[0],
      keterangan: ketIdx >= 0 ? (cols[ketIdx]||'').trim() : '',
      kategori: 'ringan',
    });
  });
  if (!importData.length) return showToast('⚠️ Tidak ada data valid di file CSV.');
  showPreviewImport();
}

function parseCsvLine(line, sep) {
  if (sep !== ',') return line.split(sep).map(c => c.replace(/^"|"$/g,'').trim());
  const result = [];
  let cur = ''; let inQuote = false;
  for (let i = 0; i < line.length; i++) {
    const c = line[i];
    if (c === '"') { inQuote = !inQuote; }
    else if (c === ',' && !inQuote) { result.push(cur.trim()); cur = ''; }
    else cur += c;
  }
  result.push(cur.trim()); return result;
}

function showPreviewImport() {
  document.getElementById('preview-info').textContent = `Ditemukan ${importData.length} baris data. Periksa sebelum diimport:`;
  const head = document.getElementById('preview-head');
  const body = document.getElementById('preview-body');
  head.innerHTML = '<th>No</th><th>Nama</th><th>Kelas</th><th>Pelanggaran</th><th style="text-align:center">Poin</th><th>Tanggal</th>';
  body.innerHTML = importData.slice(0,20).map((d,i) =>
    `<tr><td>${i+1}</td><td>${escHtml(d.nama)}</td><td>${escHtml(d.kelas)}</td><td>${escHtml(d.namaP)}</td><td class="td-poin">${d.poin}</td><td>${formatTgl(d.tanggal)}</td></tr>`
  ).join('') + (importData.length>20?`<tr><td colspan="6" style="text-align:center;color:var(--abu);font-size:12px;">... dan ${importData.length-20} baris lainnya</td></tr>`:'');
  document.getElementById('preview-import').style.display = 'block';
}

function konfirmasiImport() {
  if (!importData.length) return;
  const now = Date.now();
  const newEntries = importData.map((d,i) => ({
    id: now + i, nama: d.nama, kelas: d.kelas,
    namaP: d.namaP || 'Data diimport',
    poin: d.poin || 10,
    kategori: d.kategori || 'ringan',
    tanggal: d.tanggal || new Date().toISOString().split('T')[0],
    keterangan: d.keterangan || '',
  }));
  riwayat = [...newEntries, ...riwayat];
  simpanStorage(); updateDatalist(); renderStatusBar();
  showToast(`✅ Berhasil mengimport ${importData.length} data!`);
  batalImport();
}

function batalImport() {
  importData = [];
  document.getElementById('preview-import').style.display = 'none';
  document.getElementById('file-input-csv').value = '';
}

function downloadTemplate() {
  const csv = 'nama,kelas,poin,pelanggaran,tanggal,keterangan\nAhmad Fauzi,7A,10,Tidak mengerjakan PR,2026-06-01,Sudah diperingatkan\nSiti Rahayu,8B,5,Terlambat masuk sekolah,2026-06-02,\nBudi Santoso,9C,30,Bolos tanpa keterangan,,\n';
  downloadCSV(csv, 'template_import_siswa.csv');
}

// ============================================================
//  EXPORT
// ============================================================
function downloadCSV(csv, filename) {
  const bom = '\uFEFF';
  const blob = new Blob([bom + csv], { type:'text/csv;charset=utf-8;' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a'); a.href = url; a.download = filename; a.click();
  URL.revokeObjectURL(url);
}

function exportExcelRiwayat() {
  if (!riwayat.length) return showToast('⚠️ Belum ada data riwayat.');
  let csv = 'No,Nama Siswa,Kelas,Jenis Pelanggaran,Kategori,Poin,Tanggal,Keterangan\n';
  riwayat.forEach((r,i) => {
    csv += `${i+1},"${r.nama}","${r.kelas}","${r.namaP}","${r.kategori}",${r.poin},"${r.tanggal}","${r.keterangan||''}"\n`;
  });
  downloadCSV(csv, `riwayat_pelanggaran_smpn14_${new Date().toISOString().slice(0,10)}.csv`);
  showToast('✅ File riwayat berhasil diunduh!');
}

function exportExcelDaftar() {
  const sl = getSiswaList();
  if (!sl.length) return showToast('⚠️ Belum ada data siswa.');
  let csv = 'No,Nama Siswa,Kelas,Total Poin,Jumlah Pelanggaran,Status Sanksi\n';
  sl.forEach((s,i) => {
    const sanksi = getSanksiInfo(s.totalPoin);
    csv += `${i+1},"${s.nama}","${s.kelas}",${s.totalPoin},${s.count},"${sanksi.label}"\n`;
  });
  downloadCSV(csv, `rekap_siswa_smpn14_${new Date().toISOString().slice(0,10)}.csv`);
  showToast('✅ File rekap siswa berhasil diunduh!');
}

function backupData() {
  if (!riwayat.length) return showToast('⚠️ Belum ada data untuk di-backup.');
  const json = JSON.stringify({ versi:'1.0', exportDate: new Date().toISOString(), sekolah:'SMPN 14 Kota Tangerang', data: riwayat }, null, 2);
  const blob = new Blob([json], { type:'application/json' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a'); a.href = url;
  a.download = `backup_smpn14_${new Date().toISOString().slice(0,10)}.json`; a.click();
  URL.revokeObjectURL(url);
  showToast('✅ Backup berhasil diunduh!');
}

function restoreData(e) {
  const file = e.target.files[0]; if (!file) return;
  const reader = new FileReader();
  reader.onload = ev => {
    try {
      const parsed = JSON.parse(ev.target.result);
      const data = parsed.data || parsed;
      if (!Array.isArray(data)) throw new Error('Format tidak valid');
      if (!confirm(`Pulihkan ${data.length} data? Data yang ada TIDAK akan dihapus, data backup akan ditambahkan.`)) return;
      const ids = new Set(riwayat.map(r => r.id));
      const newData = data.filter(d => !ids.has(d.id));
      riwayat = [...newData, ...riwayat];
      simpanStorage(); updateDatalist(); renderStatusBar();
      showToast(`✅ Berhasil memulihkan ${newData.length} data!`);
    } catch(err) { showToast('⚠️ File backup tidak valid atau rusak.'); }
  };
  reader.readAsText(file);
}

function exportHTML() { window.print(); }

// ============================================================
//  TABS
// ============================================================
function showTab(name, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('tab-'+name).classList.add('active');
  btn.classList.add('active');
  if (name==='daftar')   renderDaftar();
  if (name==='riwayat')  renderRiwayat();
}
</script>
</body>
</html>
