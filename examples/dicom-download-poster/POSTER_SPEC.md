# How to View Your Medical Images: Poster Specification

A 5-step instruction poster that guides patients from the email link to their images on screen.
Style: a minimalist corporate operations manual. It uses a neutral palette with one accent color, lots of whitespace, and one action per step.

- **Format:** A3 portrait (297 × 420 mm). It also scales to A4 without layout changes.
- **Grid:** 12 columns, 20 mm outer margins, 6 mm gutters. The baseline grid is 4 mm.
- **Reference build:** `poster.html` in this folder. Open it in a browser and print to PDF at A3 with "Background graphics" turned on.

---

## 1. Text structure (final copy)

### Step 1: Overview header

| Element | Copy |
|---|---|
| Eyebrow | PATIENT GUIDE · DIGITAL IMAGING |
| Title (H1) | How to View Your Medical Images |
| Subtitle | Your scan results are in a secure OneDrive folder. It takes about 3 minutes on a Windows computer. |
| Step 1 (numbered strip) | **1 · Open the link.** Click the link in your email to open the Microsoft OneDrive folder that holds your images. |
| "Before you start" box | ☐ A Windows PC (a phone or tablet will not work) · ☐ The email from our imaging centre · ☐ Your mobile phone number (this is your password) |

### Steps 2–5: Action blocks

Each block has 3 parts: an **action title** (starting with a verb, 5 words or fewer), a **description** (1–2 sentences, 25 words or fewer), and an **image slot**. A **key detail** line is optional.

| # | Action title | Description | Key detail (accent) | Image slot |
|---|---|---|---|---|
| 2 | **Download the ZIP file** | Click the **Download** icon in the top-left corner to save the file to your computer. | Look for the ↓ arrow next to the bin icon. | **Image 2**: OneDrive preview with the Download tooltip |
| 3 | **Extract the files** | Find the downloaded ZIP file, right-click it and select **Extract All…** | Usually in your *Downloads* folder. | **Image 3**: right-click menu with "Extract All…" |
| 4 | **Enter your password** | When prompted during extraction, type your **mobile phone number** and click **OK**. | Digits only. No spaces, dashes or country code. | **Image 4**: "Password needed" dialog |
| 5 | **Open your images** | Open the extracted folder and double-click **Double click to run.BAT**. The image viewer will start. | Do not run it from inside the ZIP. Extract first. | **Image 5**: extracted folder with the .BAT file highlighted |

> Before you print, confirm with IT the exact password format (digits only, and whether a country code is included). Step 4 is where most patients get stuck.

### Footer

- **Need help?** Imaging Centre Reception · ☎ [phone] · ✉ [email] · Mon–Fri [hours]
- Safety line (small, neutral): *Only open links from emails sent by our centre. We will never ask for your password by phone or email.*
- Optional: QR code linking to a video version of this guide.

---

## 2. Visual placement instructions

```
┌────────────────────────────────────────────┐  20 mm margin
│ EYEBROW                                     │
│ How to View Your Medical Images      (H1)   │  Header zone ≈ 22% of height
│ Subtitle                                    │
│ ┌──────────────────────────────────────────┐│
│ │ (1) Open the link…   │ Before you start ☐☐☐││  Step 1 strip: accent left rule
│ └──────────────────────────────────────────┘│
├──────────── thin 0.5 pt rule ───────────────┤
│ (2) ─┬─ Title          │  ┌──────────────┐  │
│      │  Description    │  │   IMAGE 2    │  │  Each step row ≈ 16% of height
│      │  ▸ key detail   │  └──────────────┘  │
│      │                                      │
│ (3) ─┼─ …              │  [ IMAGE 3 ]       │
│      │                                      │
│ (4) ─┼─ …              │  [ IMAGE 4 ]       │
│      │                                      │
│ (5) ─┴─ …              │  [ IMAGE 5 ]       │
├─────────────────────────────────────────────┤
│ Need help? … │ safety line │ [QR]            │  Footer ≈ 6%
└────────────────────────────────────────────┘
```

**Column split (steps 2–5):**
- Columns 1–5 hold the step number and text. Columns 6–12 hold the image.
- Keep the text on the left and the image on the right in every row. Alternating sides looks dynamic, but it breaks the scan line in a procedural document.

**Vertical workflow spine:**
- A 2 pt line in neutral grey (#C9CED6) runs through the centres of the step numbers from 2 to 5.
- Step markers are 14 mm circles: accent fill with white numerals. Step 1 uses an outlined circle to show that it is the overview.

**Image slots:**
- Use one fixed frame height for every slot (≈ 42 mm on A3, the most that fits 4 rows on one page). Set images to `object-fit: contain` on a #F4F5F7 mat with a 1 pt border in #DADDE2 and a 3 mm radius.
- Crop Image 2 to its left half, which shows the toolbar and file list. At full width the 1920 px screenshot shrinks the Download icon to an unreadable size. Crop Image 5 to the file list (top ≈ 48%), because the rest is empty.
- **Callout annotations** in the accent color are the most important part of each image. Use a 2 pt ring or arrow and a small numbered badge:
  - Image 2: ring around the ↓ Download icon in the top-left.
  - Image 3: highlight bar on "Extract All…".
  - Image 4: ring around the Password field and the OK button.
  - Image 5: highlight on the "Double click to run.BAT" row.
- Blur or replace any real patient names or phone numbers in the screenshots before printing.

**Whitespace:**
- Leave at least 10 mm between step rows and 6 mm between the title and the description.
- Nothing appears between rows except the spine, so do not add dividers.

**Hierarchy check (squint test):** The H1 should read first, then the 5 accent numerals, then the action titles, then the images. Descriptions come last.

---

## 3. Color

| Token | Hex | Use |
|---|---|---|
| Ink | `#1A1D21` | Titles and body text |
| Slate | `#5B6470` | Descriptions, captions, footer |
| Line | `#DADDE2` | Rules and image borders |
| Mat | `#F4F5F7` | Image backgrounds and the "Before you start" box |
| Paper | `#FFFFFF` | Page |
| **Accent: Clinical Blue** | **`#0B5FA5`** | Step numbers, callouts, key-detail lines, Step 1 left rule |

- Use exactly one accent color and nothing else. Warnings such as the Step 4 password tip use the accent plus an icon. Do not use red, which reads as "error" in a medical setting.
- Contrast: Ink on Paper is 16.9:1. Slate on Paper is 5.9:1. Accent on Paper is 6.6:1. All pass WCAG AA, and Ink and Accent pass AAA for large text.
- The poster must still work in greyscale when photocopied. The step numerals keep enough contrast as mid-grey.

---

## 4. Typography

**Typeface:** **Inter** (or **Source Sans 3**). Use a humanist or neo-grotesque sans with tabular figures and a clear distinction between I, l and 1. This matters for the password step.
**CJK fallback:** For a Traditional Chinese edition, use **Noto Sans TC**. It matches Inter's x-height and weight axis.

| Role | Size (A3) | Weight | Leading | Tracking | Notes |
|---|---|---|---|---|---|
| Eyebrow | 11 pt | 600 | 1.2 | +12% | All caps, Accent |
| H1 title | 44 pt | 700 | 1.1 | −1% | Ink |
| Subtitle | 16 pt | 400 | 1.4 | 0 | Slate, max 60 characters per line |
| Step numeral | 22 pt | 700 | — | 0 | White in an Accent circle, tabular figures |
| Action title | 22 pt | 700 | 1.2 | −0.5% | Ink, sentence case |
| Description | 14 pt | 400 | 1.45 | 0 | Ink. **Bold** only for UI labels (Download, Extract All…, OK) |
| Key detail | 12 pt | 600 | 1.35 | 0 | Accent, preceded by ▸ |
| Image caption / label | 10 pt | 500 | 1.3 | +2% | Slate |
| Footer | 10 pt | 400 | 1.4 | 0 | Slate |

**Rules:**
- Left-align all text. Do not justify or centre it, except the step numerals.
- Keep lines to 60 characters or fewer in descriptions.
- Quote UI labels exactly as they appear on screen, including the ellipsis in "Extract All…" and the ".BAT" case, so patients can match them.
- The minimum printed size is 10 pt. For a poster read from 1–1.5 m away, the action titles should be legible from 2 m.
