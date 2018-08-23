---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588832"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Entfernt vorverarbeitet Informationen von einer [PreprocessMessage](preprocessmessage.md) Basis-Funktion aus einer Nachricht verfasst. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI-Warteschlange  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Zeiger auf die vorverarbeiteten Nachricht aus der Informationen sind, entfernt werden soll.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Vorverarbeitete Informationen wurde erfolgreich entfernt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Warteschlange Ruft eine Funktion basierend auf **RemovePreprocessInfo**. Ein Transportdienstes registriert die Funktion **RemovePreprocessInfo** basierend gleichzeitig die parallele **PreprocessMessage** Basis-Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert. 
  
Ein Bild rendern geeignet für die Übertragung von Fax ist ein Beispiel der vorverarbeiteten Informationen, die von einer Funktion, die von der [PreprocessMessage](preprocessmessage.md)Funktionsprototyp definierten geschrieben. Die MAPI-Warteschlange Ruft eine **RemovePreprocessInfo** -Funktion in der Regel nach dem Senden einer Nachricht, die vorverarbeiteten Informationen enthält. 
  

