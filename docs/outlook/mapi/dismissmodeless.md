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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565837"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI-aufrufen, wenn sie ein Dialogfeld ohne Modus Address Book geschlossen wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Clientanwendungen  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Einen implementierungsspezifischen Wert in der Regel für die Übergabe von Informationen zur Benutzeroberfläche auf eine Funktion verwendet. Beispielsweise wird in Microsoft Windows ein dieser Parameter ist das übergeordnete Fensterhandle für das Dialogfeld und vom Typ HWND in eine **ULONG_PTR**umgewandelt wird. Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert wird an die Rückruffunktion übergeben, wenn MAPI aufgerufen. Dieser Wert kann eine an die Clientanwendung Vielfache von-Adresse dar. In der Regel ist _LpvContext_ für C++-Code einen Zeiger auf die Adresse des eine C++-Objektinstanz. 
    
## <a name="return-value"></a>R�ckgabewert

Keine
  
## <a name="remarks"></a>Bemerkungen

Wenn die Client-Anwendung ein Dialogfeld ohne Modus Address Book aufruft, umfasst auch in seiner Windows Nachrichtenschleife einen Anruf an eine Funktion, die basierend auf den Prototyp [ACCELERATEABSDI](accelerateabsdi.md) , die überprüft und Zugriffstasten verarbeitet. Wenn das Dialogfeld geschlossen wird, basiert MAPI-Aufrufe, die **DISMISSMODELESS** Funktion basiert, damit die Clientanwendung angehalten wird das Aufrufen der **ACCELERATEABSDI** Funktion. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)

