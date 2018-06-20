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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 86cd30b15402f35e8396dedf6b685050ee4fb45e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791625"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Seite, die in einem Dialogfeld verwendet werden, die aus einer Tabelle anzeigen erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
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
  
> Die Position im Speicher der Zeichen Zeichenfolge Beschriftung für die Registerkarte Seite.
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung festzulegen, auf die der **UlbLpszLabelName** Member. Das folgende Flag kann festgelegt werden: 
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulbLpszComponent**
  
> Die Position im Arbeitsspeicher einer Zeichenfolge, die im Abschnitt **[Help File Mappings]** in die Datei MAPISVC identifiziert. INF-Konfigurationsdatei oder 0. Der Dateiname in die Datei MAPISVC angezeigt werden. INF-Abschnitt kann von einem Benutzer verwendet werden, um erweiterte Hilfe für die Seite zugreifen, indem Sie auf die Schaltfläche **Hilfe** klicken, im Dialogfeld. Weitere Informationen zu den Einträgen in der Datei MAPISVC. INF-Datei, finden Sie unter [File Format der Datei MAPISVC. INF-Datei](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Ein eindeutiger Bezeichner für die Seite in der Zeichenfolge, die durch das **UlbLpszComponent** -Element definiert. Das Element **UlbLpszComponent** und der **UlContext** Member müssen beide ungleich NULL für die Schaltfläche **Hilfe** zu sein. Wenn dieser Bezeichner 0 (null ist) und die Komponente Zeichenfolge NULL ist, ist keine Hilfe mit der Seite verknüpft ist. 
    
## <a name="remarks"></a>Hinweise

Eine Struktur **DTBLPAGE** beschreibt eine Seite ein Steuerelement, das verwendet wird, um mehrere zugehörige Dialogfelder zu trennen. In der Regel werden diese Dialogfelder Eigenschaftenseiten für die Konfiguration, Nachricht oder Empfänger Optionen anzeigen. Durch Klicken auf die Registerkarte, kann der Benutzer von einem Arbeitsblatt wechseln. 
  
Die Komponente Zeichenfolge und Kontext-ID finden Sie Informationen, ob erweiterte Hilfe für die Seite verfügbar ist. Wenn erweiterte Hilfe verfügbar ist, bietet die Komponente Zeichenfolge und Kontext-ID Informationen dazu, wie Sie darauf zugreifen. Die Komponente Zeichenfolge ordnet der Hilfedatei. die Kontext-ID wird die ursprüngliche Hilfethema zugeordnet. Wenn die Kontext-ID 0 (null ist) und die Komponente Zeichenfolge NULL ist, ist die erweiterte Hilfe nicht verfügbar.
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

