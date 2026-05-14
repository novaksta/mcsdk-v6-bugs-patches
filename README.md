# mcsdk-v6-bugs-patches
My repository for gathering bugs, patches and tricks for MCSDK v6.4.2 (by now)

## 1. Trick/patch H533 Nucleo:
  The difinition of the board is missing possibility to use certain pins (PB1 at MR24) to use most of the boards (IHM09 + classic-floppy-MC-connector).
  In repo is [trick file](NUCLEO-H533RE.json).

## 2. ACIM problems
  ### 2.1. generation
  #### 2.1.1 HL/EN enable pins are not possible way
  #### 2.1.2 Open-loop not possible and not out-of the box
  #### 2.1.3 LSO debug (VF) does nothing
  ### 2.2 LSO
  #### 2.2.1 when non 1pp motor LSO not seem working well 
    When 2pp motor OL voltage at 1000rpm mechanical, LSO is giving 500 rpm.
  ### 2.2.2 Some variable isnisde LSO seem used from previous RUN 
    TODO find Which
  ### 2.3 No good GUI for ACIM and registers not ready for ACIM

## 3. profiler problem
  ### 3.1 GUI is wore than v5
    THsi can be fixed -- TODO upload here.
  ### F3 profiler issue
    When getting to limit (HF 25kHz) we may get to situation that max current is not determiders corectly. This is due to safety task is has lowest priority and SCC do not checks MOE bit but internal variable (when preempted by MF screwed...).
    
