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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795395"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange Ruft eine Funktion basierend auf **RemovePreprocessInfo**. Ein Transportdienstes registriert die Funktion **RemovePreprocessInfo** basierend gleichzeitig die parallele **PreprocessMessage** Basis-Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert. 
  
Ein Bild rendern geeignet für die Übertragung von Fax ist ein Beispiel der vorverarbeiteten Informationen, die von einer Funktion, die von der [PreprocessMessage](preprocessmessage.md)Funktionsprototyp definierten geschrieben. Die MAPI-Warteschlange Ruft eine **RemovePreprocessInfo** -Funktion in der Regel nach dem Senden einer Nachricht, die vorverarbeiteten Informationen enthält. 
  

