# HYDROS Repository Setup Guide

## Step 1: Create Repository ✅ DONE
- Repository name: `HYDROS`
- Owner: sxennn
- Visibility: Public
- URL: https://github.com/sxennn/HYDROS

## Step 2: Add Repository Description
Go to **Settings** → **About** → **Description** and paste:

```
Self-sustaining underwater life support station extracting dissolved O2 
from seawater for 6 divers at 20m depth. No tanks. No surface supply. 
NEMO Labs 2026.
```

## Step 3: Add Topics
Go to **Settings** → **Topics** and add:
- `underwater-engineering`
- `membrane-technology`
- `oxygen-extraction`
- `scuba`
- `life-support`
- `henry-law`
- `fick-law`
- `betz-law`
- `autocad`
- `simscale`

## Step 4: Upload Folder Structure

Create these folders (or they will auto-create when you add files):

```
HYDROS/
├── docs/
│   ├── HYDROS_Complete_PSR_Package.docx
│   ├── HYDROS_Technical_Manual.docx
│   └── HYDROS_Technical_Calculations.docx
├── cad/
│   ├── HYDROS_MASTER.dwg
│   └── drawings/
│       ├── A101_Front_Elevation.pdf
│       ├── A101_Section_AA.pdf
│       └── A101_Manifold_Detail.pdf
├── simulation/
│   ├── SimScale_CFD/
│   ├── SimScale_FEA/
│   └── PhET_screenshots/
├── calculations/
│   └── computation_sheet.pdf
└── README.md
```

## Step 5: File Upload Method Options

### Option A: Upload via GitHub Web UI (Easiest)
1. Click **Add file** → **Upload files**
2. Drag & drop files or click to select
3. Use commit messages from `COMMIT_MESSAGES.md`
4. Commit to main branch

### Option B: Git Command Line (Faster for bulk)
```bash
git clone https://github.com/sxennn/HYDROS.git
cd HYDROS

# Organize files into folders
mkdir -p docs cad/drawings simulation/SimScale_CFD simulation/SimScale_FEA calculations

# Copy your files into these folders
# Then commit and push:

git add .
git commit -m "Add PSR package, technical manual, and calculations (docs/)"
git push origin main
```

### Option C: Git LFS for Large Files
If HYDROS_MASTER.dwg exceeds GitHub limits:
```bash
git lfs install
git lfs track "*.dwg"
git add .gitattributes
git add cad/HYDROS_MASTER.dwg
git commit -m "Add AutoCAD master file and engineering drawings (cad/)"
git push origin main
```

## Step 6: Enable Discussions (Optional)
Go to **Settings** → **Features** → Enable **Discussions** for team collaboration.

## Step 7: Verify Repository
Once all files are uploaded:
- ✅ README.md displays correctly on repo homepage
- ✅ All folders visible in file tree
- ✅ Description and topics appear in About section
- ✅ Issue templates available when creating issues

---

**File Size Warning:**
- HYDROS_MASTER.dwg (AutoCAD): Typically 2-15 MB
  - GitHub limit: 100 MB per file
  - If larger, use Git LFS or split into smaller drawings
- PDF drawings: Usually 0.5-3 MB each (no issues)
- DOCX files: Usually 1-5 MB each (no issues)

**Total typical repo size:** 50-150 MB (well within GitHub's free tier limits)

---

Team: Famaran, Cordova, Manabat, Ancheta — NEMO Labs May 2026
