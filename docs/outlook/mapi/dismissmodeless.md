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
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428186"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI aufruft, wenn sie ein Dialogfeld für ein modusloses Adressbuch verworfen hat. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der in der Regel zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Microsoft Windows ist dieser Parameter beispielsweise das übergeordnete Fensterhandle für das Dialogfeld und hat den Typ HWND, wird in ein **ULONG_PTR.** Der Wert Null gibt an, dass kein übergeordnetes Fenster besteht. 
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft. Dieser Wert kann eine Für die Clientanwendung wichtige Adresse darstellen. In der Regel ist  _lpvContext_ für C++-Code ein Zeiger auf die Adresse einer C++-Objektinstanz. 
    
## <a name="return-value"></a>Rückgabewert

Keine
  
## <a name="remarks"></a>Hinweise

Wenn die Clientanwendung ein Dialogfeld ohne Adressbuch aufruft, enthält sie in der Windows-Nachrichtenschleife einen Aufruf einer Funktion basierend auf dem [ACCELERATEABSDI-Prototyp,](accelerateabsdi.md) der nach Zugriffstasten sucht und diese verarbeitet. Wenn das Dialogfeld geschlossen wird, ruft MAPI die **DISMISSMODELESS-basierte** Funktion auf, sodass die Clientanwendung den Aufruf der **ACCELERATEABSDI-basierten** Funktion beendet. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)

