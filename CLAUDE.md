# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Problem-Based Learning (PBL) educational repository** for the "Parabolas for Profit" project, designed for high school Algebra 2/Pre-Calculus students. The project teaches mathematical optimization through real-world business scenarios where students help local restaurants determine optimal pricing strategies.

**Core Question:** "How can we help a local business make the most money?"

## Repository Structure

The repository follows a numbered directory structure representing the chronological flow of the 19-day project:

- `00_TEACHER_PLANNING_AND_RESOURCES/` - Planning documents, calendars, rubrics, and restaurant menu JSON files
- `01_PROJECT_LAUNCH_AND_SETUP/` - Entry event materials and team formation templates
- `02_MATH_LESSONS_AND_MODULES/` - Mathematical lessons on regression, break-even analysis, and optimization
- `03_DATA_AND_SURVEY_MATERIALS/` - Synthetic pricing datasets and survey templates
- `04_FINAL_PRODUCT_FILES_AND_REPORTS/` - Student deliverable templates
- `05_ASSESSMENT_AND_RUBRICS/` - Grading rubrics and evaluation tools
- `ZZ_STUDENT_EXEMPLARS/` - Sample completed student work

## Key Data Files

### Restaurant Menu Files (JSON)
Located in `00_TEACHER_PLANNING_AND_RESOURCES/`:
- `goldenmonkey_menu.json` - Golden Monkey Cafe (Cambodian cuisine)
- `mandees_menu.json` - Mandee's Pizza (Italian)
- `yaschicken_menu.json` - Yas Chicken (Korean fusion)

Structure: Contains restaurant info and nested menu categories with items, descriptions, and prices.

### Synthetic Datasets (CSV)
Located in `03_DATA_AND_SURVEY_MATERIALS/DATA_Synthetic_Datasets/`:
- `DATA_GoldenMonkey_BubbleTea.csv`
- `DATA_MandeesPizza_Specialty.csv`
- `DATA_YasChicken_Combo.csv`

CSV Structure: `business, price_usd, demand_customers, variable_cost_per_item_usd, fixed_cost_per_day_usd, revenue_usd, total_cost_usd, profit_usd`

### Vocabulary Gamification (CSV)
- `02_MATH_LESSONS_AND_MODULES/GAME_Blooket_Vocab_Import.csv` - 23 business/math terms for Blooket game

## Common Development Tasks

### Working with Menu Data
When modifying or analyzing menu JSON files:
1. Maintain the existing structure with `restaurant` and `menu` top-level keys
2. Ensure all prices are numeric values (not strings)
3. Keep descriptions under 200 characters for readability

### Working with Pricing Datasets
When creating or modifying CSV datasets:
1. Maintain exactly 36 rows of data
2. Calculate revenue as: `price_usd * demand_customers`
3. Calculate total cost as: `(variable_cost_per_item_usd * demand_customers) + fixed_cost_per_day_usd`
4. Calculate profit as: `revenue_usd - total_cost_usd`
5. Ensure demand follows a realistic downward-sloping pattern with price

### Creating New Business Scenarios
To add a new restaurant/business:
1. Create a menu JSON file following the existing format
2. Generate a synthetic dataset with 36 price points
3. Ensure the profit function forms a parabola (quadratic relationship)
4. Set realistic fixed costs ($100-500/day) and variable costs (20-40% of price)

## Mathematical Models

The project uses these core formulas:
- **Demand Function:** `D(p) = mp + b` (linear, negative slope)
- **Revenue Function:** `R(p) = p × D(p)`
- **Cost Function:** `C(p) = variable_cost × D(p) + fixed_cost`
- **Profit Function:** `P(p) = R(p) - C(p)` (quadratic)
- **Optimal Price:** Vertex of profit parabola where `p = -b/2a`

## File Naming Conventions

- **Planning docs:** `PLAN_[Description].[ext]`
- **Reference materials:** `REF_[Topic].[ext]`
- **Templates:** `TPL_[Purpose].[ext]`
- **Lessons:** `LESSON_[Topic].[ext]`
- **Modules:** `MOD_M[#]_[Topic].[ext]`
- **Data files:** `DATA_[Business]_[Product].csv`
- **Exemplars:** `EX_[Type]_[Business].[ext]`
- **Surveys:** `SURVEY_[Purpose].[ext]`
- **Worksheets:** `WKS_[Topic].[ext]`
- **Rubrics:** `RUBRIC_[Version].[ext]`

## Project Timeline

The project follows a 19-day sequence:
- **Days 1-4:** Launch, team formation, survey design
- **Days 5-8:** Data collection and demand analysis
- **Days 9-12:** Mathematical modeling and optimization
- **Days 13-16:** Report development and peer feedback
- **Days 17-19:** Presentations and reflection

## Important Notes

- This is an educational repository, not a software development project
- No build, test, or deployment processes exist
- Files are primarily documents (DOCX, PDF, XLSX) and data files (JSON, CSV)
- The project integrates with external tools: Google Forms/Sheets, Desmos Calculator, Blooket
- All restaurant data is from real businesses in the greater Boston area
- Synthetic datasets are pre-generated to ensure mathematical relationships work properly