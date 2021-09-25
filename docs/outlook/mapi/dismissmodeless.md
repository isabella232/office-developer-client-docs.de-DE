---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bc1921f1761754cab47ec1b478957bffbad63119
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556784"
---
# <a name="dismissmodeless"></a>DISMISSMODELESS

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die mapi aufruft, wenn ein Dialogfeld ohne Modus adressbuch geschlossen wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der in der Regel zum Übergeben von Benutzeroberflächeninformationen an eine Funktion verwendet wird. In Microsoft Windows ist dieser Parameter beispielsweise das übergeordnete Fensterhandle für das Dialogfeld und hat den Typ HWND und wird in eine **ULONG_PTR** umgewandelt. Der Wert Null gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn die MAPI sie aufruft. Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung von Bedeutung ist. In der Regel ist  _lpvContext_ für C++-Code ein Zeiger auf die Adresse einer C++-Objektinstanz. 
    
## <a name="return-value"></a>Rückgabewert

Keines
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Clientanwendung ein Dialogfeld ohne Adressbuch aufruft, enthält sie in ihrer Windows Meldungsschleife einen Aufruf einer Funktion basierend auf dem [ACCELERATEABSDI-Prototyp,](accelerateabsdi.md) der Zugriffstasten überprüft und verarbeitet. Wenn das Dialogfeld geschlossen wird, ruft MAPI die **AUF SCHLIEßENMODELESS** basierende Funktion auf, sodass die Clientanwendung den Aufruf der **AUF BESCHLEUNIGUNGABSDI** basierenden Funktion beendet. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)

