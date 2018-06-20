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
ms.openlocfilehash: dc830665f425b747d2fdb05641dc037a2e84f695
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791564"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Betrifft**: Outlook 
  
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
  
## <a name="remarks"></a>Hinweise

Wenn die Client-Anwendung ein Dialogfeld ohne Modus Address Book aufruft, umfasst auch in seiner Windows Nachrichtenschleife einen Anruf an eine Funktion, die basierend auf den Prototyp [ACCELERATEABSDI](accelerateabsdi.md) , die überprüft und Zugriffstasten verarbeitet. Wenn das Dialogfeld geschlossen wird, basiert MAPI-Aufrufe, die **DISMISSMODELESS** Funktion basiert, damit die Clientanwendung angehalten wird das Aufrufen der **ACCELERATEABSDI** Funktion. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)

