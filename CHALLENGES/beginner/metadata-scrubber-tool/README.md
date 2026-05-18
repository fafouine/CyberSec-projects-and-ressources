# Metadata Scrubber Tool

**Difficulty:** Beginner  
**Time Estimate:** 6-8 hours  
**Languages:** Python, Go  
**Topics:** File formats, metadata extraction, privacy protection, image processing

## Challenge Description

Build a tool that removes sensitive metadata from files (EXIF from images, timestamps, author info, etc.). This protects privacy and removes information that could identify location, device, or system details from shared files.

## Learning Objectives

- [ ] Understand metadata in different file formats (JPEG, PNG, PDF, Office)
- [ ] Extract EXIF data from images
- [ ] Remove metadata while preserving file content
- [ ] Handle multiple file formats
- [ ] Batch process files
- [ ] Verify metadata removal

## Requirements

### Functional Requirements
- Remove EXIF data from JPEG images
- Remove metadata from PNG images
- Remove metadata from PDF documents
- Remove metadata from Office documents (DOCX, XLSX)
- Support batch processing (multiple files/directories)
- Preserve file integrity after cleaning
- Generate report of removed metadata
- Verify metadata removal
- Backup original files (optional)

### Non-Functional Requirements
- Performance: Process 100MB directory in <1 minute
- Reliability: No file corruption
- Safety: Option to backup originals

## Acceptance Criteria

- [ ] Removes EXIF data from JPEG files
- [ ] Removes metadata from PNG files
- [ ] Removes metadata from PDF files
- [ ] Removes metadata from DOCX/XLSX files
- [ ] File remains readable after cleaning
- [ ] Batch processing works correctly
- [ ] Reports removed metadata accurately
- [ ] Handles errors gracefully
- [ ] Well-documented code

## Getting Started

### Option 1: Build from Scratch
1. Research file format structures
2. Learn about EXIF data in JPEGs
3. Implement EXIF removal
4. Add PNG metadata handling
5. Add PDF support
6. Add Office document support
7. Implement batch processing
8. Add verification

### Option 2: Use Starter Code
```bash
cd starter_code
# Follow the README.md in starter_code/
```

### Option 3: Learn from Solution
```bash
cd solution
# Review reference implementations
```

## Metadata Types by Format

### JPEG/EXIF
- Camera make, model
- GPS coordinates
- Date/time taken
- ISO, shutter speed, aperture
- User comments

### PNG
- Text chunks (author, copyright, description)
- Creation time
- Comments

### PDF
- Title, author
- Subject, keywords
- Creation/modification date
- Producer software
- Embedded metadata

### Office (DOCX, XLSX)
- Author, company
- Last modified by
- Creation/modification times
- Comments and tracked changes

## Python Libraries

- **Pillow (PIL):** Image handling
- **piexif:** EXIF data
- **PyPDF2/pypdf:** PDF manipulation
- **python-docx:** DOCX handling
- **openpyxl:** Excel handling

## Tips & Hints

- **EXIF removal:** Strip EXIF during image re-encoding
- **Verify removal:** Read file again to confirm metadata is gone
- **Batch processing:** Use recursive directory traversal
- **Backups:** Copy files to backup directory before modification
- **Test files:** Use sample images with visible EXIF data
- **GPS data:** Show coordinates in human-readable format (lat/lon)

## Testing Your Solution

```bash
# View metadata before cleaning
python metadata_scrubber.py --view photo.jpg

# Remove metadata from single file
python metadata_scrubber.py --clean photo.jpg -o photo_clean.jpg

# Batch clean directory
python metadata_scrubber.py --clean /path/to/files/ --recursive

# Verify removal
python metadata_scrubber.py --verify photo_clean.jpg

# Generate report
python metadata_scrubber.py --report removed_metadata.json
```

## Further Learning

- **Related challenge:** [Steganography Multi-Tool](../steganography-multi-tool/)
- **Privacy:** Understand privacy implications of metadata
- **Real tools:** Study ExifTool, ImageMagick, ghostscript
- **Advanced:** Implement metadata obfuscation (fake data)

## Extensions

- [ ] GUI interface for batch cleaning
- [ ] Automatic detection of sensitive metadata
- [ ] Metadata archival (save removed data)
- [ ] Comparison between original and cleaned
- [ ] Real-time file monitoring

## Rubric

| Criteria | Points | Notes |
|----------|--------|-------|
| Format Support | 40% | JPEG, PNG, PDF, Office all work |
| Accuracy | 20% | Removes all relevant metadata |
| Batch Processing | 15% | Handles multiple files/dirs |
| Code Quality | 15% | Clean, readable, documented |
| Reliability | 10% | No file corruption, handles errors |

---

[Back to Challenge List](../../README.md)
