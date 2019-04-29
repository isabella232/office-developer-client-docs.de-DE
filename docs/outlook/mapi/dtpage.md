---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408222"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt das Dialogfeld, das von der [BuildDisplayTable](builddisplaytable.md) -Funktion aus einer Anzeigetabelle erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>Members

 **cctl**
  
> Die Anzahl der Steuerelemente, auf die durch das **lpctl** -Element verwiesen wird. 
    
 **lpszResourceName**
  
> Zeiger auf den Namen oder ganzzahligen Bezeichner für die Dialogfeldressource. 
    
 **lpszComponent**
  
> Zeiger auf die Zeichenfolge, die im Abschnitt **[Hilfedatei Zuordnungen]** in MAPISVC. inf angezeigt wird. Da sich **lpszComponent** in einer Union mit dem **ulItemID** -Element befindet, verfügt nur einer dieser Member über gültige Daten. 
    
 **ulItemID**
  
> Integer-Ressourcenbezeichner mit einem Wert kleiner oder gleich 65535, aus dem der Name der Hilfedatei gelesen werden kann. Da sich **ulItemID** in einer Union mit dem **lpszComponent** -Element befindet, verfügt nur einer dieser Member über gültige Daten. 
    
 **lpctl**
  
> Zeiger auf ein Array von [DTCTL](dtctl.md) -Strukturen, eines für jedes Steuerelement auf der Seite. 
    
## <a name="remarks"></a>Bemerkungen

Um die Hilfedatei für die Registerkartenseite zu identifizieren, legen Sie entweder das **lpszComponent** -Element auf eine hart codierte Zeichenfolge oder das **ulItemID** -Element auf einen ganzzahligen Ressourcenbezeichner fest. 
  
Jeder Eintrag im Abschnitt **[Hilfedatei Zuordnungen]** in MAPISVC. INF besteht aus einer Komponenten Zeichenfolge, die nicht länger als 30 Zeichen ist, auf der linken Seite und einem Pfad rechts für die Hilfedatei. Sowohl **ulItemID** als auch **lpszResourceName** befinden sich im _HINSTANCE_ -Parameter von **BuildDisplayTable**. Weitere Informationen finden Sie unter [MAPISVC. Abschnitt "INF [Hilfedatei Zuordnungen]"](mapisvc-inf-help-file-mappings-section.md).
  
Obwohl **BuildDisplayTable** diese Struktur verwendet, um die Anzeigetabelle aus den Steuerelementressourcen zu erstellen, wird die **DTPAGE** -Struktur nie in der Anzeigetabelle selbst angezeigt. 
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

