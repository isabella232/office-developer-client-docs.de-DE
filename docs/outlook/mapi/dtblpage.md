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
  
Beschreibt eine Registerkartenseite, die in einem Dialogfeldverwendet wird, das aus einer Anzeigetabelle erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
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
  
> Position im Speicher der Zeichenfolgenbezeichnung für die Registerkarte Seite.
    
 **ulFlags**
  
> Bitmaske der Flags, mit denen das Format der Bezeichnung festgelegt wird, auf die durch das **ulbLpszLabelName** -Element verwiesen wird. Das folgende Flag kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulbLpszComponent**
  
> Position im Speicher einer Zeichenfolge, die den Abschnitt **[Hilfedatei Zuordnungen]** im Mapisvc identifiziert. INF-Konfigurationsdatei oder 0. Der Dateiname, der im MAPISVC angezeigt wird. Der Abschnitt INF kann von Benutzern verwendet werden, um auf die erweiterte Hilfe für die Registerkartenseite zuzugreifen, indem Sie im Dialogfeld auf die Schaltfläche " **Hilfe** " klicken. Weitere Informationen zu den Einträgen in MAPISVC. INF finden Sie unter [Datei Format von MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Ein eindeutiger Bezeichner für die Registerkartenseite in der vom **ulbLpszComponent** -Element definierten Zeichenfolge. Das **ulbLpszComponent** -Element und das **ulContext** -Element müssen beide ungleich NULL sein, damit die Schaltfläche " **Hilfe** " funktioniert. Wenn dieser Bezeichner NULL ist und die Komponenten Zeichenfolge NULL ist, ist der Seite keine Hilfe zugeordnet. 
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLPAGE** -Struktur beschreibt ein Steuerelement mit Registerkarten, das zum Trennen mehrerer verwandter Dialogfelder verwendet wird. In der Regel sind diese Dialogfelder Eigenschaftenblätter zum Anzeigen von Konfigurations-, Nachrichten-oder Empfängeroptionen. Durch Klicken auf die Registerkarte kann der Benutzer von einem Blatt zu einem anderen wechseln. 
  
Die Komponenten Zeichenfolge und die Kontext-ID enthalten Informationen darüber, ob die erweiterte Hilfe für die Registerkartenseite verfügbar ist. Wenn die erweiterte Hilfe verfügbar ist, enthält die Komponenten Zeichenfolge und die Kontext-ID Informationen dazu, wie Sie darauf zugreifen können. Die Komponenten Zeichenfolge wird der Hilfedatei zugeordnet; der Kontextbezeichner wird dem anfänglichen Hilfethema zugeordnet. Wenn der Kontextbezeichner NULL ist und die Komponenten Zeichenfolge NULL ist, ist die erweiterte Hilfe nicht verfügbar.
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

