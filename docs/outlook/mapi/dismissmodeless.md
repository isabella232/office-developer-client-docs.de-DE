---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339774"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die von MAPI aufgerufen wird, wenn ein Dialogfeld für nicht modale Adressbücher geschlossen wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Client Anwendungen  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein implementierungsspezifischer Wert, der normalerweise zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Microsoft Windows ist dieser Parameter beispielsweise das übergeordnete Fensterhandle für das Dialogfeld und vom Typ HWND und wird in einen **ULONG_PTR**umgewandelt. Der Wert 0 (null) gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvContext_
  
> in Zeiger auf einen beliebigen Wert, der beim Aufrufen von MAPI an die Rückruffunktion übergeben wird. Dieser Wert kann eine für die Clientanwendung bedeutsame Adresse darstellen. Für C++-Code ist _LpvContext_ in der Regel ein Zeiger auf die Adresse einer c++-Objektinstanz. 
    
## <a name="return-value"></a>Rückgabewert

Keine
  
## <a name="remarks"></a>Bemerkungen

Wenn die Clientanwendung ein nicht modales Adressbuch-Dialogfeld aufruft, enthält es in der Windows-Meldungsschleife einen Aufruf an eine auf dem [ACCELERATEABSDI](accelerateabsdi.md) -Prototyp basierende Funktion, die Zugriffstasten überprüft und verarbeitet. Wenn das Dialogfeld geschlossen ist, ruft MAPI die **DISMISSMODELESS** -basierte Funktion auf, sodass die Clientanwendung den Aufruf der **ACCELERATEABSDI** -basierten Funktion beendet. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)

