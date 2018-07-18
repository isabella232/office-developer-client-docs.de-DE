---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791635"
---
# <a name="dtctl"></a>DTCTL

**Betrifft**: Outlook 
  
Beschreibt ein Steuerelement, das in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Elemente

**ulCtlType**
  
> Typ des Steuerelements, die in der **Ctl** -Element enthalten ist, und **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Mögliche Werte sind wie folgt:
    
DTCT_LABEL 
  
> Bezeichnungsfeld-Steuerelement.
    
DTCT_EDIT 
  
> Edit-Steuerelement.
    
DTCT_LBX 
  
> Listenfeld-Steuerelement.
    
DTCT_COMBOBOX 
  
> Kombinationsfeld-Steuerelement.
    
DTCT_DDLBX 
  
> Dropdown-Listenfeld-Steuerelement.
    
DTCT_CHECKBOX 
  
> Kontrollkästchen-Steuerelement.
    
DTCT_GROUPBOX 
  
> Gruppenfeld-Steuerelement.
    
DTCT_BUTTON 
  
> Schaltflächen-Steuerelement.
    
DTCT_PAGE 
  
> Mit Registerkarten-Seitensteuerelement.
    
DTCT_RADIOBUTTON 
  
> Optionsfeld-Steuerelement.
    
DTCT_MVLISTBOX 
  
> Mehrwertiges Listenfeld-Steuerelement.
    
DTCT_MVDDLBX 
  
> Mehrwertiges Dropdown-Listenfeld-Steuerelement.
    
**ulCtlFlags**
  
> Bitmaske aus Flags, die Beschreibung des Steuerelements Features und **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Diese Flags für Kontrollkästchen, Kombinationsfelder und Listenfelder festgelegt werden können, und Steuerelemente nur bearbeiten. Mögliche Werte sind wie folgt:
    
DT_ACCEPT_DBCS 
  
> Die ANSI oder DBCS-Format wird akzeptiert. Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.
    
DT_EDITABLE 
  
> Benutzer können den Text im Steuerelement ändern. 
    
DT_MULTILINE 
  
> Das Steuerelement kann mehrere Textzeilen enthalten. Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.
    
DT_PASSWORD_EDIT 
  
> Das Steuerelement enthält ein Kennwort an. Daher sollte der Inhalt des Steuerelements nicht dem Benutzer angezeigt werden. Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.
    
DT_REQUIRED 
  
> Das Dialogfeld-Steuerelement ist erforderlich. Dieses Kennzeichen gilt nur für bearbeiten und Kombinationsfeld-Steuerelemente.
    
DT_SET_IMMEDIATE 
  
> Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung des Steuerelements. Dies ermöglicht eine abhängigkeitsbeziehung zwischen zwei Steuerelemente eingerichtet werden. 
    
**lpbNotif**
  
> Zeiger auf eine Struktur, die eine [GUID](guid.md) -Struktur zur Darstellung der Dienstanbieter und einen Bezeichner für das Steuerelement besteht. Die Member **LpbNotif** und **CbNotif** **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements entspricht und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement hat aktualisiert werden.
    
**cbNotif**
  
> Anzahl von Bytes in der Struktur auf den Member **LpbNotif** zeigt. 
    
**lpszFilter**
  
> Zeiger auf eine Zeichenfolge, die beschreibt, welche Zeichen in einer bearbeiten oder Kombinationsfeld-Steuerelement eingegeben werden können. Für andere Arten von Steuerelementen kann der **LpszFilter** Member NULL sein. Für bearbeiten und Kombinationsfeld-Steuerelemente sollten sie ein regulärer Ausdruck sein, der auf einem einzelnen Zeichen zu einem Zeitpunkt angewendet wird. Der gleiche Filter wird auf alle Zeichen im Steuerelement angewendet. Das Format der Filterzeichenfolge lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> | Ein beliebiges Zeichen ist zulässig (z. B. `"*"`).  <br/> |
| `[ ]` <br/> |Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"`.)  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen (z. B. `"[a-z]"`).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (beispielsweise `"[~0-9]")`. <br/>|   
| `\` <br/> |Verwendet, um die vorherigen Zeichen quote (z. B. `"[\-\\\[\]]"` bedeutet-, \, [, und] Zeichen sind zulässig).  <br/> |
   
**ulItemID**
  
> Wert, der das Steuerelement in das Dialogfeld Feld Ressource identifiziert. Für Seiten mit Registerkarten-Steuerelemente des Typs der **UlItemID** DTCT_PAGE wird Mitglied optional den Namen der Komponente für die Seite aus einer String-Ressource zu laden. Position und Beschriftung Informationen werden aus dem Dialogfeld Feld Ressource gelesen. 
    
**CTL**
  
> Eine Struktur, die die Daten für das Steuerelement enthält und **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Jede Art von Steuerelement verfügt über eine andere Struktur.
    
## <a name="remarks"></a>Bemerkungen

Die Struktur **DTCTL** beschreibt ein Steuerelement eines beliebigen Typs. Die meisten ihrer Member werden verwendet, um Eigenschaften für das Steuerelement festzulegen. 
  
Der **Ctl** -Member ist eine Vereinigung von Strukturen, die mit einer bestimmten Art von Steuerelement verknüpft sind. Wenn die **DTCTL** -Struktur, die ein Bearbeitungssteuerelement beschreibt ist, zeigen auf eine [DTBLEDIT](dtbledit.md) -Struktur beispielsweise der **Ctl** Member. Diese Struktur entspricht **PR_CONTROL_STRUCTURE** -Eigenschaft des Steuerelements. Die Union hat eine Variable vom Typ LPVOID kompilieren Zeit Initialisierung der Struktur **DTCTL** als erste Member. 
  
Obwohl die [BuildDisplayTable](builddisplaytable.md) -Funktion die **DTCTL** -Struktur für die Erstellung von der Tabelle anzeigen von Steuerelementressourcen verwendet wird, wird die Struktur **DTCTL** nie in der Anzeige Tabelle selbst angezeigt. Diese Struktur stellt nur Informationen zu **BuildDisplayTable**bereit.
  
In der **UlCtlFlags** -Member Bearbeitungssteuerelemente vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT wirkt sich nur. Zwei andere DT_REQUIRED und DT_SET_IMMEDIATE Einfluss auf ein beliebiges Steuerelement bearbeitet werden. 
  
Die Steuerelemente für ein Dialogfeld verfügbar sind Label, Textfeld, Ink-fähigen Textfeld, Liste, Dropdown-Listenfeld, Kombinationsfeld, das Kontrollkästchen, Gruppenfeld, Schaltfläche, Optionsfeld und Seite mit Registerkarten.
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [MAPI-Strukturen](mapi-structures.md)

