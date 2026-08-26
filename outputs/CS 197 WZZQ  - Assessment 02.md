# CS 197 WZZQ - Assessment 02

Submitted by Stephen Singer (2019-05493) on August 23, 2026.
## Linked Lists

*Given a linked list pointed to by $l$*

![[Pasted image 20260823133740.png]]

*and a new node pointed by $\alpha$*

![[Pasted image 20260823133726.png]]

## Append Left

*Write an algorithm to insert the new node at the head of the list:, i.e. node $\alpha$ becomes the first node of list $l$.*

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

*Write an algorithm to insert the new node at the tail of the list, i.e. node $\alpha$ becomes the last node of list $l$.*

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

*Assume that the nodes in list l are sorted in increasing order of the contents of the $INFO$ field, i.e. $x_1 < x_2 < x_3 < \ldots < x_n$. Write an algorithm to insert the new node into the list such that the list remains sorted.*

```pseudo
\begin{algorithm} 
\begin{algorithmic}
	\Procedure{SORTED_INSERT}{$l, \alpha$} 
		\If{$l = \Lambda$ or \Call{INFO}{$\alpha$} $\le$ \Call{INFO}{$l$}} 
			\State $LINK(\alpha) \gets l$
			\State $l \gets \alpha$
			\Return
		\EndIf
		
		\State $p \gets l$
		
		\While{\Call{LINK}{p} $\ne \Lambda$ and \Call{INFO}{\Call{LINK}{p}} $\le$ \Call{INFO}{$\alpha$}}		
			\State $p \gets$ \Call{LINK}{$p$}
		\EndWhile
		
		\State \Call{LINK}{$\alpha$} $\gets$ \Call{LINK}{$p$}
		\State \Call{LINK}{$p$} $\gets \alpha$
		 
	\EndProcedure 
\end{algorithmic}
\end{algorithm}
```

## Graphs

*This section refers to the following table mapping courses to students enlisted:*

![[Pasted image 20260823143944.png]]

### Graph Drawing

*Draw the graph which represents the relevant information to solve the exam-scheduling problem for the class lists given below.*


The table can be transposed to emphasize the students present in the courses.

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


To spot conflicts easily, the table can be sorted alphabetically.

$$ {\small \begin{array}{*{12}{l}} \text{\textbf{C01}} & \text{\textbf{C02}} & \text{\textbf{C03}} & \text{\textbf{C04}} & \text{\textbf{C05}} & \text{\textbf{C06}} & \text{\textbf{C07}} & \text{\textbf{C08}} & \text{\textbf{C09}} & \text{\textbf{C10}} & \text{\textbf{C11}} & \text{\textbf{C12}} \\ \text{ADB} & \text{BEB} & \text{BSM} & \text{BBI} & \text{BBB} & \text{BCI} & \text{BCB} & \text{BWU} & \text{BOA} & \text{BCC} & \text{BBI} & \text{BMB} \\ \text{BKC} & \text{CLC} & \text{BWU} & \text{BQR} & \text{CBX} & \text{DEC} & \text{BCT} & \text{CCC} & \text{DBB} & \text{BEG} & \text{BEG} & \text{CNG} \\ \text{BMG} & \text{CNG} & \text{DMC} & \text{CDF} & \text{CCD} & \text{EIJ} & \text{BLL} & \text{DEW} & \text{ERQ} & \text{BLL} & \text{CDG} & \text{FEF} \\ \text{BTK} & \text{CTT} & \text{FDG} & \text{DTM} & \text{CEZ} & \text{FTM} & \text{BMA} & \text{FED} & \text{FSR} & \text{CCD} & \text{EEY} & \text{FHN} \\ \text{EPS} & \text{CUK} & \text{FHN} & \text{ECU} & \text{EIJ} & \text{GCM} & \text{BMQ} & \text{FMG} & \text{HDF} & \text{CDL} & \text{FEF} & \text{FTT} \\ \text{KLS} & \text{DMC} & \text{FNJ} & \text{FHG} & \text{ERQ} & \text{JTH} & \text{CDF} & \text{FMY} & \text{HMH} & \text{ECU} & \text{KHP} & \text{JWL} \\ \text{LGM} & \text{FQS} & \text{KPK} & \text{KDA} & \text{FDG} & \text{KMS} & \text{FQR} & \text{FNJ} & \text{KDA} & \text{FTZ} & \text{LMS} & \text{LTO} \\ \text{NOH} & \text{ISH} & \text{MFQ} & \text{KFT} & \text{IMA} & \text{MPT} & \text{HMH} & \text{FQS} & \text{MMM} & \text{HDF} & \text{MHM} & \text{MHM} \\ \text{OBC} & \text{LMS} & \text{NOH} & \text{LMO} & \text{IMH} & \text{NBV} & \text{IHN} & \text{ITE} & \text{NBN} & \text{JFY} & \text{MSQ} & \text{OBC} \\ \text{ODT} & \text{MHM} & \text{OBC} & \text{NDA} & \text{ODT} & \text{QFP} & \text{KHP} & \text{JTH} & \text{NBV} & \text{KHP} & \text{NDA} & \text{PEP} \\ \text{SDE} & \text{RKP} & \text{OGM} & \text{SFR} & \text{SFW} & \text{SNN} & \text{LFV} & \text{KFI} & \text{OBC} & \text{NJN} & \text{SMM} & \text{SEA} \\ \text{UKF} & \text{TEE} & \text{SDN} & \text{STP} & \text{SPN} & \text{UFX} & \text{NDA} & \text{PEP} & \text{QFP} & \text{SBW} & \text{SSK} & \text{WJV} \\ \text{WDB} & \text{VLF} & \text{SEA} & \text{XJL} & \text{USY} & \text{WJR} & \text{SPN} & \text{SFR} & \text{SFW} & \text{STQ} & \text{TMF} & \text{WMJ} \\ \text{YNZ} & \text{XEB} & \text{STP} & \text{YUK} & \text{UYO} & \sim & \text{ZFZ} & \text{SSK} & \text{TFT} & \sim & \text{XBR} & \sim \\ \sim & \text{YNZ} & \text{ZJR} & \sim & \text{XSE} & \sim & \sim & \text{UQL} & \text{WMJ} & \sim & \sim & \sim \end{array} } $$

To visually show the conflicts between courses, the table is converted to its sparse representation. The conflicts are outlined as shown below:

$$
{ 	{\small
	    \begin{array}{*{12}{l}}
	    \hline
	        \textbf{C01} & \textbf{C02} & \textbf{C03} & \textbf{C04} & \textbf{C05} & \textbf{C06} & \textbf{C07} & \textbf{C08} & \textbf{C09} & \textbf{C10} & \textbf{C11} & \textbf{C12} \\ \hline
	        ADB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & BBB & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & BBI & ~ & ~ & ~ & ~ & ~ & ~ & BBI & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & BCB & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BCC & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & BCI & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & BCT & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & BEB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BEG & BEG & ~ \\ \hline 
	        BKC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & BLL & ~ & ~ & BLL & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & BMA & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BMB \\ 
	        BMG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & BMQ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & BOA & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & BQR & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & BSM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        BTK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & BWU & ~ & ~ & ~ & ~ & BWU & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & CBX & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & CCC & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & CCD & ~ & ~ & ~ & ~ & CCD & ~ & ~ \\ \hline
	        ~ & ~ & ~ & CDF & ~ & ~ & CDF & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CDG & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CDL & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & CEZ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & CLC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & CNG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & CNG \\ \hline
	        ~ & CTT & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\
	        ~ & CUK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & DBB & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & DEC & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & DEW & ~ & ~ & ~ & ~ \\ \hline
	        ~ & DMC & DMC & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline 
	        ~ & ~ & ~ & DTM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ECU & ~ & ~ & ~ & ~ & ~ & ECU & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & EEY & ~ \\ \hline
	        ~ & ~ & ~ & ~ & EIJ & EIJ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        EPS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ERQ & ~ & ~ & ~ & ERQ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & FDG & ~ & FDG & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\  \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FED & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FEF & FEF \\ \hline
	        ~ & ~ & ~ & FHG & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & FHN & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FHN \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FMG & ~ & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & FMY & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & FNJ & ~ & ~ & ~ & ~ & FNJ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & FQR & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & FQS & ~ & ~ & ~ & ~ & ~ & FQS & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FSR & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & FTM & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FTT \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & FTZ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & GCM & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & HDF & HDF & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & HMH & ~ & HMH & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & IHN & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & IMA & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & IMH & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ISH & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ITE & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & JFY & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & JTH & ~ & JTH & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & JWL \\ \hline
	        ~ & ~ & ~ & KDA & ~ & ~ & ~ & ~ & KDA & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & KFI & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & KFT & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & KHP & ~ & ~ & KHP & KHP & ~ \\ \hline
	        KLS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & KPK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & KMS & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & LFV & ~ & ~ & ~ & ~ & ~ \\ 
	        LGM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & LMO & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & LMS & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & LMS & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & LTO \\ 
	        ~ & ~ & MFQ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & MHM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MHM & MHM \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MMM & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & MPT & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & MSQ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & NBN & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & NBV & ~ & ~ & NBV & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & NDA & ~ & ~ & NDA & ~ & ~ & ~ & NDA & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & NJN & ~ & ~ \\ \hline
	        NOH & ~ & NOH & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        OBC & ~ & OBC & ~ & ~ & ~ & ~ & ~ & OBC & ~ & ~ & OBC \\ \hline
	        ODT & ~ & ~ & ~ & ODT & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & OGM & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & PEP & ~ & ~ & ~ & PEP \\ \hline
	        ~ & ~ & ~ & ~ & ~ & QFP & ~ & ~ & QFP & ~ & ~ & ~ \\ \hline
	        ~ & RKP & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SBW & ~ & ~ \\ 
	        SDE & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & SDN & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & SEA & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SEA \\ \hline
	        ~ & ~ & ~ & SFR & ~ & ~ & ~ & SFR & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & SFW & ~ & ~ & ~ & SFW & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & SNN & ~ & ~ & ~ & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & ~ & SPN & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & SPN & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & SMM & ~ \\ 
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & SSK & ~ & ~ & SSK & ~ \\\hline
	        ~ & ~ & STP & STP & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
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
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & WJV \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & WMJ & ~ & ~ & WMJ \\ \hline
	        ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & XBR & ~ \\ 
	        ~ & XEB & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ~ & XJL & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\         
		~ & ~ & ~ & ~ & XSE & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        YNZ & YNZ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ \hline
	        ~ & ~ & ~ & YUK & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\
	        ~ & ~ & ~ & ~ & ~ & ~ & ZFZ & ~ & ~ & ~ & ~ & ~ \\ 
	        ~ & ~ & ZJR & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ & ~ \\ 
	    \end{array}} }
$$


With the earlier table, the following list of intersections is confirmed. There are a total of 35 unique conflicts between the courses.

| Course A | Course B | Student       |
| -------- | -------- | ------------- |
| 1        | 2        | YNZ           |
| 1        | 3        | NOH           |
| 1        | 5        | ODT           |
| 1        | 9        | OBC           |
| 1        | 12       | OBC           |
| 2        | 3        | DMC           |
| 2        | 8        | FQS           |
| 2        | 11       | CNG, LMS, MHM |
| 2        | 12       | MHM           |
| 3        | 4        | STP           |
| 3        | 5        | FDG           |
| 3        | 8        | BWU           |
| 3        | 9        | OBC           |
| 3        | 12       | FHN, OBC, SEA |
| 4        | 6        | NDA           |
| 4        | 7        | CDF           |
| 4        | 8        | SFR           |
| 4        | 9        | KDA           |
| 4        | 10       | ECU           |
| 4        | 11       | BBI, NDA      |
| 5        | 9        | ERQM SFW      |
| 5        | 10       | EIJ, CCD      |
| 6        | 8        | JTH           |
| 6        | 9        | NBV, QFP      |
| 6        | 11       | NDA           |
| 7        | 9        | HMH           |
| 7        | 10       | BLL, KHP      |
| 7        | 11       | KHP           |
| 7        | 12       | KHP           |
| 8        | 11       | SSK           |
| 8        | 12       | PEP           |
| 9        | 10       | HDF           |
| 9        | 12       | OBC, WMJ      |
| 10       | 12       | BEG, KHP      |
| 11       | 12       | FEF           |

The same table can be represented as a graph wherein the vertices are the courses and the connections are the conflicts.

![[conflict.png]]
### Graph Coloring with G Algorithm

*Apply Algorithm G to color the graph. Is the coloring optimal?*

Here are the notes and the state of the graph for each iteration of Algorithm G.

#### Step 1

The first color is applied to C01. The unconnected vertices are C04, C07, C08, C10,  and C11. However, upon coloring C04, the other unconnected vertices will conflict with C04 so only two vertices can be colored for the first step.

![[1.png]]


#### Step 2

The second color is applied to C02. The unconnected vertices are C05,C 06, C07, C09,  and C10. However, C05 conflicts with C09 and C10 so only C02, C05, C06, and C07 were colored for the second step.

![[2.png]]

#### Step 3

The third color is applied to C03. The unconnected vertices are C10 and C11 for a total of three newly colored vertices.

![[3.png]]
#### Step 4

Skipping the already colored nodes, the fourth color is applied to C08. The only other unconnected vertex is C9, for a total of two newly colored vertices.

![[4.png]]
#### Step 5

Finally, the last vertex to be colored is C12.
![[5.png]]

In total, there are five colors required to color all the vertices with the G algorithm. Returning to the context of the scheduling program, five time slots will be made if the algorithm is followed.

The graph requires at least four colors.
- A one-color solution is impossible because at least one edge exists in the graph. For example, C01 and C02 are adjacent and therefore cannot share the same color.
- A two-color solution is impossible because the graph contains a triangle formed by C01, C02, and C03. Since each vertex in a triangle is adjacent to the other two, at least three colors are required.
- A three-color solution is impossible because the graph contains a complete subgraph of four vertices: C01, C03, C09, and C12. Since every pair of vertices in this subgraph is adjacent, four distinct colors are required.

Therefore, the number of colors needed for the graph is at least four. Given the G algorithm has produced a solution of 5 colors, the optimal answer is either 4 or 5.  

To determine whether the graph is actually colorable with just four colors, it is not sufficient to examine the result of a single greedy ordering. One approach would be to consider all $12!$ possible vertex orderings and apply the greedy algorithm to each. However, this would be impractical.

Instead, a backtracking algorithm can be used to directly test whether a valid 4-coloring exists. In the worst case, there are $4^{12}$ possible assignments of four colors to the twelve vertices. In practice, the search space is much smaller because any partial assignment that creates a conflict between adjacent vertices is immediately discarded. As a result, many impossible colorings are eliminated before they are fully explored. If a valid 4-coloring is found, then the graph can be colored using four colors; otherwise, five colors are required.


```python
from collections import defaultdict  
  
edges = [  
	(1,2),(1,3),(1,5),(1,9),(1,12),  
	(2,3),(2,8),(2,11),(2,12),  
	(3,4),(3,5),(3,8),(3,9),(3,12),  
	(4,6),(4,7),(4,8),(4,9),(4,10),(4,11),  
	(5,9),(5,10),  
	(6,8),(6,9),(6,11),  
	(7,9),(7,10),(7,11),(7,12),  
	(8,11),(8,12),  
	(9,10),(9,12),  
	(10,12),  
	(11,12)  
]  

# Dictionary of sets to quickly check for adjacency
adjacent = defaultdict(set)  

for u, v in edges:  
	adjacent[u].add(v)  
	adjacent[v].add(u)  

# Focus on cases with multiple adjacent vertices first so contradiction appear quickly
# But not really needed for solution
vertices = sorted(adjacent,  key=lambda vertex: len(adjacent[vertex]), reverse=True)

def solve():  

	coloring = {}  
	
	def is_valid_color(vertex, proposed_color):  
		return not any(
			coloring.get(neighbor) == proposed_color  
			for neighbor in adjacent[vertex]  
		)
	
	def backtrack(depth):  
		
		# All vertices colored successfully
		if depth == len(vertices):  
			return coloring.copy()  
		
		vertex = vertices[depth]  
		
		for color in range(4):  
			# None of the neighbors use this color
			if is_valid_color(vertex, color):  
				coloring[vertex] = color  
		
				result = backtrack(depth + 1)
				if result is not None:  
					return result  
		
				# Undo assignment and try another color
				del coloring[vertex]
		
		# Failure
		return None  

	# Actually solve
	return backtrack(0)


solution = solve()  
if solution:  
	print("4-coloring exists") 
	print(solution)
else:
	print("No 4-coloring exists") 
```

The code used above (assuming it's correct and has no unforeseen bugs), shows there is no 4-color solution. Therefore, the G algorithm has provided an optimal solution. However, this does not necessarily mean the algorithm itself is optimal.

### Unoptimized Algorithm

*Algorithm G is a greedy algorithm in that it tries to color as many uncolored vertices as it legally can with the current color before turning to another color. The idea is that this will result in as few colors as possible. Show that this technique does not necessary yield an optimal coloring for the graph.*

Let's assume the G algorithm is optimized such that it will always give the lowest amount of colors required for a given graph. If one case shows it doesn't generate the lowest amount of colors, then by proof of contradiction it is not an optimized solution.

Consider this reshuffled graph that maintains the same connections. This permutation was found after some trial and error. For emphasis, the numbers are retained from the original graph. Algorithm G will go through this graph left to right under the assumption it is numbered 01 to 12 in its perspective.



![[b.png]]



#### Step 1

Applying the first color to C01, the remaining unconnected vertices are C04, C06, C07, C08, C10, and C11. Coloring C06 prevents C04, C08, and C11 from being colored. Coloring C07 prevents C10 from being colored. In total, the first step can color three vertices at most without conflicts.


![[b1.png]]

#### Step 2

Coloring Course 09, the remaining unconnected vertices are C8 and C11. However, coloring C11 blocks C8. In total, the second step can color two vertices at most.


![[b2.png]]

#### Step 3


Coloring C03, the remaining unconnected vertex is C10. The third step can color three vertices at most.


![[b3.png]]

#### Step 4

Coloring C12, the remaining unconnected vertices are C04 and C05. In total, a maximum of three vertices can be colored.


![[b4.png]]

#### Step 5

Now, purely following the rules of the G algorithm, C08 must be given a new color. There are no more unconnected vertices left with respect to C08. For this, only one vertex can be colored in this step.


![[b5.png]]


#### Step 6

Finally, while still following the G algorithm, the last vertex to be colored is C02. 

![[b6.png]]

The application of the G algorithm for the same graph in a different arrangement result in six colors. The order of the vertices matter for the final result despite the problem having a clear optimal solution of 4-5 colors. Thus, the G algorithm is not always optimal.