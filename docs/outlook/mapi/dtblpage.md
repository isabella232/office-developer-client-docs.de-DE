---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424000"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Registerkartenseite, die in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a>Elemente

 **ulbLpszLabel**
  
> Position im Arbeitsspeicher der Zeichenzeichenfolgenbeschriftung für die Seitenregisterkarte.
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf das das **ulbLpszLabelName-Element** verweist. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
 **ulbLpszComponent**
  
> Position im Arbeitsspeicher einer Zeichenzeichenfolge, die **den Abschnitt [Hilfedateizuordnungen]** im MAPISVC identifiziert. INF-Konfigurationsdatei oder 0. Der Dateiname, der im MAPISVC angezeigt wird. Der ABSCHNITT "INF" kann von einem Benutzer verwendet werden,  um auf die erweiterte Hilfe für die Registerkartenseite zu zugreifen, indem er im Dialogfeld auf die Schaltfläche Hilfe klickt. Weitere Informationen zu den Einträgen in MAPISVC. INF, siehe [Dateiformat von MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Ein eindeutiger Bezeichner für die Registerkartenseite in der vom **ulbLpszComponent-Element definierten Zeichenfolge.** Das **ulbLpszComponent-Element** und das **ulContext-Element** müssen beide ungleich Null sein, damit die Schaltfläche **Hilfe** funktioniert. Wenn dieser Bezeichner null ist und die Komponentenzeichenfolge NULL ist, ist der Seite keine Hilfe zugeordnet. 
    
## <a name="remarks"></a>Hinweise

Eine **DTBLPAGE-Struktur** beschreibt eine Registerkartenseite ein Steuerelement, das zum Trennen mehrerer zugehöriger Dialogfelder verwendet wird. In der Regel handelt es sich bei diesen Dialogfelder um Eigenschaftenblätter zum Anzeigen von Konfigurations-, Nachrichten- oder Empfängeroptionen. Durch Klicken auf die Registerkarte kann der Benutzer von einem Blatt zu einem anderen wechseln. 
  
Die Komponentenzeichenfolge und der Kontextbezeichner enthalten Informationen dazu, ob die erweiterte Hilfe für die Registerkartenseite verfügbar ist. Wenn erweiterte Hilfe verfügbar ist, enthalten die Komponentenzeichenfolge und der Kontextbezeichner Informationen zum Zugriff darauf. Die Komponentenzeichenfolge ordnet der Hilfedatei zu. der Kontextbezeichner dem ersten Hilfethema zu ordnet. Wenn der Kontextbezeichner null und die Komponentenzeichenfolge NULL ist, ist erweiterte Hilfe nicht verfügbar.
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

