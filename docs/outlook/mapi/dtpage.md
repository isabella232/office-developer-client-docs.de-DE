---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0bf031772c9dda44e0496f507975f26313aa452e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576331"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt das Dialogfeld, das von der [BuildDisplayTable-Funktion](builddisplaytable.md) aus einer Anzeigetabelle erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
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
  
> Anzahl der Steuerelemente, auf die vom **lpctl-Element** verwiesen wird. 
    
 **lpszResourceName**
  
> Zeiger auf den Namen oder ganzzahligen Bezeichner für die Dialogfeldressource. 
    
 **lpszComponent**
  
> Zeiger auf die Zeichenfolge, die im Abschnitt **[Help File Mappings]** in MAPISVC.INF angezeigt wird. Da **lpszComponent** sich in einer Vereinigung mit dem **ulItemID-Element** befindet, verfügt nur eines dieser Member über gültige Daten. 
    
 **ulItemID**
  
> Ganzzahliger Ressourcenbezeichner mit einem Wert kleiner oder gleich 65535, aus dem der Name der Hilfedatei gelesen werden kann. Da **sich ulItemID** in einer Vereinigung mit dem **LpszComponent-Element** befindet, verfügt nur eines dieser Member über gültige Daten. 
    
 **lpctl**
  
> Zeiger auf ein Array von [DTCTL-Strukturen,](dtctl.md) eine für jedes Steuerelement auf der Seite. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Um die Hilfedatei für die Registerkartenseite zu identifizieren, legen Sie entweder das **Element lpszComponent** auf eine hartcodierte Zeichenfolge oder das **UlItemID-Element** auf einen ganzzahligen Ressourcenbezeichner fest. 
  
Jeder Eintrag im Abschnitt **[Hilfedateizuordnungen]** in MAPISVC. INF besteht aus einer Komponentenzeichenfolge, die nicht mehr als 30 Zeichen umfasst, auf der linken Seite und einem Hilfedateipfad auf der rechten Seite. Sowohl **ulItemID** als auch **lpszResourceName** befinden sich im _hInstance-Parameter_ von **BuildDisplayTable.** Weitere Informationen finden Sie unter [MAPISVC. INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).
  
Obwohl **BuildDisplayTable** diese Struktur verwendet, um die Anzeigetabelle aus Steuerelementressourcen zu erstellen, wird die **DTPAGE-Struktur** nie in der Anzeigetabelle selbst angezeigt. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

