# CS 197 WZZQ - Assessment 02

Submitted by Stephen Singer (2019-05493) on August 23, 2026.
## Linked Lists

Given a linked list pointed to by $l$
![[Pasted image 20260823133740.png]]
and a new node pointed by $\alpha$
![[Pasted image 20260823133726.png]]

## Append Left

Write an algorithm to insert the new node at the head of the list:, i.e. node $\alpha$ becomes the first node of list $l$.

```pseudo
\begin{algorithm} 
\begin{algorithmic} 
	\Procedure{APPEND_LEFT}{$l, \alpha$} 
		\State $LINK(\alpha) \gets l$
		\State $l \gets \alpha$
	\EndProcedure 
\end{algorithmic}
\end{algorithm}
```

### Append Right

Write an algorithm to insert the new node at the tail of the list, i.e. node $\alpha$ becomes the last node of list $l$.

```pseudo
\begin{algorithm} 
\begin{algorithmic} 

	\Procedure{GET_TAIL}{$l$} 	
	\If{$l = \Lambda$} 
		\Return $l$  	
	\EndIf 
	
	\State $t \gets l$
	\While{\Call{LINK}{$t$} $\ne \Lambda$}
		\State $t \gets$ \Call{LINK}{$t$}
	\EndWhile
	\Return t
	\EndProcedure 

	\Procedure{APPEND_RIGHT}{$l, \alpha$} 
		\State \Call{LINK}{$\alpha$} $\gets \Lambda$ 
		\If{$l = \Lambda$} 
			\State $l \gets \alpha$ 
		\Else 
			\State $t \gets$ \Call{GET_TAIL}{$l$}
			\State \Call{LINK}{$t$} $\gets \alpha$ 	
		\EndIf 
	\EndProcedure 
	
\end{algorithmic}
\end{algorithm}
```
### Sorted Insert
Assume that the nodes in list l are sorted in increasing order of the contents of the $INFO$ field, i.e. $x_1 < x_2 < x_3 < \ldots < x_n$. Write an algorithm to insert the new node into the list such that the list remains sorted.
```pseudo
\begin{algorithm} 
\begin{algorithmic}
	\Procedure{SORTED_INSERT}{$l, \alpha$} 
		\State $x_{\alpha} \gets $ \Call{INFO}{$\alpha$} 
	\EndProcedure 
\end{algorithmic}
\end{algorithm}
```

## Graphs

This section refers to the following table mapping courses to students enlisted:
![[Pasted image 20260823143944.png]]

### Graph Drawing

Draw the graph which represents the relevant information to solve the exam-scheduling problem for the class lists given below.


The table can be transposed to the following form:

$$
{\small
\begin{array}{*{12}{l}}
    \text{\textbf{C01}} & \text{\textbf{C02}} & \text{\textbf{C03}} & \text{\textbf{C04}} & \text{\textbf{C05}} & \text{\textbf{C06}} & \text{\textbf{C07}} & \text{\textbf{C08}} & \text{\textbf{C09}} & \text{\textbf{C10}} & \text{\textbf{C11}} & \text{\textbf{C12}} \\
    \text{ADB} & \text{BEB} & \text{SEA} & \text{NDA} & \text{BBB} & \text{DEC} & \text{BMA} & \text{CCC} & \text{BOA} & \text{BCC} & \text{NDA} & \text{SEA} \\
    \text{WDB} & \text{XEB} & \text{OBC} & \text{KDA} & \text{IMA} & \text{JTH} & \text{NDA} & \text{FED} & \text{KDA} & \text{CCD} & \text{FEF} & \text{BMB} \\
    \text{BKC} & \text{CLC} & \text{DMC} & \text{CDF} & \text{CCD} & \text{BCI} & \text{BCB} & \text{ITE} & \text{DBB} & \text{HDF} & \text{TMF} & \text{OBC} \\
    \text{OBC} & \text{DMC} & \text{FDG} & \text{FHG} & \text{XSE} & \text{EIJ} & \text{CDF} & \text{FMG} & \text{OBC} & \text{BEG} & \text{BEG} & \text{FEF} \\
    \text{SDE} & \text{TEE} & \text{NOH} & \text{BBI} & \text{FDG} & \text{FTM} & \text{HMH} & \text{JTH} & \text{HDF} & \text{BLL} & \text{CDG} & \text{CNG} \\
    \text{UKF} & \text{VLF} & \text{FNJ} & \text{YUK} & \text{IMH} & \text{GCM} & \text{BLL} & \text{KFI} & \text{HMH} & \text{CDL} & \text{BBI} & \text{WMJ} \\
    \text{BMG} & \text{CNG} & \text{KPK} & \text{XJL} & \text{EIJ} & \text{SNN} & \text{IHN} & \text{FNJ} & \text{WMJ} & \text{NJN} & \text{SSK} & \text{JWL} \\
    \text{NOH} & \text{ISH} & \text{BSM} & \text{DTM} & \text{SPN} & \text{QFP} & \text{SPN} & \text{SSK} & \text{MMM} & \text{KHP} & \text{MHM} & \text{MHM} \\
    \text{BTK} & \text{CUK} & \text{OGM} & \text{LMO} & \text{UYO} & \text{WJR} & \text{KHP} & \text{UQL} & \text{NBN} & \text{STQ} & \text{SMM} & \text{FHN} \\
    \text{LGM} & \text{MHM} & \text{FHN} & \text{STP} & \text{ERQ} & \text{KMS} & \text{BMQ} & \text{PEP} & \text{QFP} & \text{ECU} & \text{KHP} & \text{LTO} \\
    \text{EPS} & \text{RKP} & \text{SDN} & \text{BQR} & \text{ODT} & \text{MPT} & \text{FQR} & \text{SFR} & \text{ERQ} & \text{JFY} & \text{MSQ} & \text{PEP} \\
    \text{KLS} & \text{FQS} & \text{STP} & \text{SFR} & \text{SFW} & \text{NBV} & \text{BCT} & \text{FQS} & \text{FSR} & \text{SBW} & \text{XBR} & \text{FTT} \\
    \text{ODT} & \text{LMS} & \text{MFQ} & \text{KFT} & \text{CBX} & \text{UFX} & \text{LFV} & \text{BWU} & \text{TFT} & \text{FTZ} & \text{LMS} & \text{WJV} \\
    \text{YNZ} & \text{CTT} & \text{ZJR} & \text{ECU} & \text{USY} & \sim & \text{ZFZ} & \text{DEW} & \text{NBV} & \sim & \text{EEY} & \sim \\
    \sim & \text{YNZ} & \text{BWU} & \sim & \text{CEZ} & \sim & \sim & \text{FMY} & \text{SFW} & \sim & \sim & \sim
\end{array}
}
$$


The table can then be organized alphabetically as shown:

$$ {\small \begin{array}{*{12}{l}} \text{\textbf{C01}} & \text{\textbf{C02}} & \text{\textbf{C03}} & \text{\textbf{C04}} & \text{\textbf{C05}} & \text{\textbf{C06}} & \text{\textbf{C07}} & \text{\textbf{C08}} & \text{\textbf{C09}} & \text{\textbf{C10}} & \text{\textbf{C11}} & \text{\textbf{C12}} \\ \text{ADB} & \text{BEB} & \text{BSM} & \text{BBI} & \text{BBB} & \text{BCI} & \text{BCB} & \text{BWU} & \text{BOA} & \text{BCC} & \text{BBI} & \text{BMB} \\ \text{BKC} & \text{CLC} & \text{BWU} & \text{BQR} & \text{CBX} & \text{DEC} & \text{BCT} & \text{CCC} & \text{DBB} & \text{BEG} & \text{BEG} & \text{CNG} \\ \text{BMG} & \text{CNG} & \text{DMC} & \text{CDF} & \text{CCD} & \text{EIJ} & \text{BLL} & \text{DEW} & \text{ERQ} & \text{BLL} & \text{CDG} & \text{FEF} \\ \text{BTK} & \text{CTT} & \text{FDG} & \text{DTM} & \text{CEZ} & \text{FTM} & \text{BMA} & \text{FED} & \text{FSR} & \text{CCD} & \text{EEY} & \text{FHN} \\ \text{EPS} & \text{CUK} & \text{FHN} & \text{ECU} & \text{EIJ} & \text{GCM} & \text{BMQ} & \text{FMG} & \text{HDF} & \text{CDL} & \text{FEF} & \text{FTT} \\ \text{KLS} & \text{DMC} & \text{FNJ} & \text{FHG} & \text{ERQ} & \text{JTH} & \text{CDF} & \text{FMY} & \text{HMH} & \text{ECU} & \text{KHP} & \text{JWL} \\ \text{LGM} & \text{FQS} & \text{KPK} & \text{KDA} & \text{FDG} & \text{KMS} & \text{FQR} & \text{FNJ} & \text{KDA} & \text{FTZ} & \text{LMS} & \text{LTO} \\ \text{NOH} & \text{ISH} & \text{MFQ} & \text{KFT} & \text{IMA} & \text{MPT} & \text{HMH} & \text{FQS} & \text{MMM} & \text{HDF} & \text{MHM} & \text{MHM} \\ \text{OBC} & \text{LMS} & \text{NOH} & \text{LMO} & \text{IMH} & \text{NBV} & \text{IHN} & \text{ITE} & \text{NBN} & \text{JFY} & \text{MSQ} & \text{OBC} \\ \text{ODT} & \text{MHM} & \text{OBC} & \text{NDA} & \text{ODT} & \text{QFP} & \text{KHP} & \text{JTH} & \text{NBV} & \text{KHP} & \text{NDA} & \text{PEP} \\ \text{SDE} & \text{RKP} & \text{OGM} & \text{SFR} & \text{SFW} & \text{SNN} & \text{LFV} & \text{KFI} & \text{OBC} & \text{NJN} & \text{SMM} & \text{SEA} \\ \text{UKF} & \text{TEE} & \text{SDN} & \text{STP} & \text{SPN} & \text{UFX} & \text{NDA} & \text{PEP} & \text{QFP} & \text{SBW} & \text{SSK} & \text{WJV} \\ \text{WDB} & \text{VLF} & \text{SEA} & \text{XJL} & \text{USY} & \text{WJR} & \text{SPN} & \text{SFR} & \text{SFW} & \text{STQ} & \text{TMF} & \text{WMJ} \\ \text{YNZ} & \text{XEB} & \text{STP} & \text{YUK} & \text{UYO} & \sim & \text{ZFZ} & \text{SSK} & \text{TFT} & \sim & \text{XBR} & \sim \\ \sim & \text{YNZ} & \text{ZJR} & \sim & \text{XSE} & \sim & \sim & \text{UQL} & \text{WMJ} & \sim & \sim & \sim \end{array} } $$

Furthermore, the table can be represented as a sparce table: 
$$
	{\small
    \begin{array}{*{12}{l}}
    \hline
        \textbf{C01} & \textbf{C02} & \textbf{C03} & \textbf{C04} & \textbf{C05} & \textbf{C06} & \textbf{C07} & \textbf{C08} & \textbf{C09} & \textbf{C10} & \textbf{C11} & \textbf{C12} \\ \hline
        ADB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & BBB & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & BBI & ~ & ~ & ~ & ~ & ~ & ~ & BBI & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & BCB & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BCC & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & BCI & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & BCT & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & BEB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BEG & BEG & ~ \\ 
        BKC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & BLL & ~ & ~ & BLL & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & BMA & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BMB \\ 
        BMG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & BMQ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BOA & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & BQR & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & BSM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        BTK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & BWU & ~ & ~ & ~ & ~ & BWU & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & CBX & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & CCC & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & CCD & ~ & ~ & ~ & ~ & CCD & ~ & ~ \\ 
        ~ & ~ & ~ & CDF & ~ & ~ & CDF & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CDG & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CDL & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & CEZ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & CLC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & CNG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CNG \\ 
        ~ & CTT & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & CUK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & DBB & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & DEC & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & DEW & ~ & ~ & ~ & ~ \\ 
        ~ & DMC & DMC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & DTM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ECU & ~ & ~ & ~ & ~ & ~ & ECU & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & EEY & ~ \\ 
        ~ & ~ & ~ & ~ & EIJ & EIJ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        EPS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ERQ & ~ & ~ & ~ & ERQ & ~ & ~ & ~ \\ 
        ~ & ~ & FDG & ~ & FDG & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FED & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FEF & FEF \\ 
        ~ & ~ & ~ & FHG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & FHN & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FHN \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FMG & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FMY & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & FNJ & ~ & ~ & ~ & ~ & FNJ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & FQR & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & FQS & ~ & ~ & ~ & ~ & ~ & FQS & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FSR & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & FTM & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FTT \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FTZ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & GCM & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & HDF & HDF & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & HMH & ~ & HMH & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & IHN & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & IMA & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & IMH & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ISH & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ITE & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & JFY & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & JTH & ~ & JTH & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & JWL \\ 
        ~ & ~ & ~ & KDA & ~ & ~ & ~ & ~ & KDA & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & KFI & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & KFT & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & KHP & ~ & ~ & KHP & KHP & ~ \\ 
        KLS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & KPK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & KMS & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & LFV & ~ & ~ & ~ & ~ & ~ \\ 
        LGM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & LMO & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & LMS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & LMS & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & LTO \\ 
        ~ & ~ & MFQ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & MHM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MHM & MHM \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MMM & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & MPT & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MSQ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & NBN & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & NBV & ~ & ~ & NBV & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & NDA & ~ & ~ & NDA & ~ & ~ & ~ & NDA & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & NJN & ~ & ~ \\ 
        NOH & ~ & NOH & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        OBC & ~ & OBC & ~ & ~ & ~ & ~ & ~ & OBC & ~ & ~ & OBC \\ 
        ODT & ~ & ~ & ~ & ODT & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & OGM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & PEP & ~ & ~ & ~ & PEP \\ 
        ~ & ~ & ~ & ~ & ~ & QFP & ~ & ~ & QFP & ~ & ~ & ~ \\ 
        ~ & RKP & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SBW & ~ & ~ \\ 
        SDE & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & SDN & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & SEA & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SEA \\ 
        ~ & ~ & ~ & SFR & ~ & ~ & ~ & SFR & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & SFW & ~ & ~ & ~ & SFW & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & SNN & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & SPN & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & SPN & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SMM & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & SSK & ~ & ~ & SSK & ~ \\
        ~ & ~ & STP & STP & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & STQ & ~ & ~ \\ 
        ~ & TEE & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & TFT & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & TMF & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & UFX & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        UKF & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & UQL & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & USY & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & UYO & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & VLF & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        WDB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & WJR & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & WJV \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & WMJ & ~ & ~ & WMJ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & XBR & ~ \\ 
        ~ & XEB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & XJL & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\         
	~ & ~ & ~ & ~ & XSE & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        YNZ & YNZ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & YUK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ~ & ~ & ~ & ~ & ZFZ & ~ & ~ & ~ & ~ & ~ \\ 
        ~ & ~ & ZJR & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
    \end{array}}
$$


This leaves the following table of intersection:



### G Algorithm

Apply Algorithm G to color the graph. Is the coloring optimal?

### Unoptimized Algorithm

Algorithm G is a greedy algorithm in that it tries to color as many uncolored vertices as it legally can with the current color before turning to another color. The idea is that this will result in as few colors as possible.. Show that this technique does not necessary yield an optimal coloring for the graph.
