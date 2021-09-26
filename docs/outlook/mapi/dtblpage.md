---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60c84f90c483261fa1feb888f065cbf1b9409a88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630957"
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

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position im Speicher der Zeichenfolgenbeschriftung für die Registerkarte "Seite".
    
 **ulFlags**
  
> Bitmaske mit Kennzeichen, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf die der **UlbLpszLabelName-Member** verweist. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
 **ulbLpszComponent**
  
> Position im Speicher einer Zeichenfolge, die den Abschnitt **[Hilfedateizuordnungen]** in MAPISVC identifiziert. INF-Konfigurationsdatei oder 0. Der Dateiname, der in MAPISVC angezeigt wird. Der INF-Abschnitt kann von einem Benutzer verwendet werden, um auf die erweiterte Hilfe für die Registerkartenseite zuzugreifen, indem er im Dialogfeld auf die **Schaltfläche "Hilfe"** klickt. Weitere Informationen zu den Einträgen in MAPISVC. INF, see [File Format of MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Ein eindeutiger Bezeichner für die Registerkartenseite in der Zeichenfolge, die vom **ulbLpszComponent-Element** definiert wird. Der **ulbLpszComponent-Member** und das **ulContext-Element** müssen beide ungleich Null sein, damit die **Hilfeschaltfläche** funktioniert. Wenn dieser Bezeichner Null und die Komponentenzeichenfolge NULL ist, ist der Seite keine Hilfe zugeordnet. 
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLPAGE-Struktur** beschreibt eine Registerkartenseite eines Steuerelements, das zum Trennen mehrerer verwandter Dialogfelder verwendet wird. In der Regel sind diese Dialogfelder Eigenschaftenblätter zum Anzeigen von Konfigurations-, Nachrichten- oder Empfängeroptionen. Durch Klicken auf die Registerkarte kann der Benutzer von einem Blatt zu einem anderen wechseln. 
  
Die Komponentenzeichenfolge und der Kontextbezeichner enthalten Informationen darüber, ob die erweiterte Hilfe für die Registerkartenseite verfügbar ist. Wenn die erweiterte Hilfe verfügbar ist, enthält die Komponentenzeichenfolge und der Kontextbezeichner Informationen zum Zugriff darauf. Die Komponentenzeichenfolge ist der Hilfedatei zugeordnet. Der Kontextbezeichner ist dem anfänglichen Hilfethema zugeordnet. Wenn der Kontextbezeichner Null und die Komponentenzeichenfolge NULL ist, ist die erweiterte Hilfe nicht verfügbar.
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

