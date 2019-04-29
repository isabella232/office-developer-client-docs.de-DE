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
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432947"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt vorverarbeitete Informationen, die von einer [PreprocessMessage](preprocessmessage.md) -basierten Funktion geschrieben wurden, aus einer Nachricht. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Transport Anbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI-Spooler  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> in Zeiger auf die vorverarbeitete Nachricht, von der die Informationen entfernt werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Vorverarbeitete Informationen wurden erfolgreich entfernt.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler Ruft eine auf **RemovePreprocessInfo**basierende Funktion auf. Ein Transportanbieter registriert die **RemovePreprocessInfo** -basierte Funktion bei der Registrierung der parallelen **PreprocessMessage** -basierten Funktion bei einem Aufruf der [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode. 
  
Ein für die Fax-Übertragung geeignetes Bildrendering ist ein Beispiel für vorverarbeitete Informationen, die von einer durch den [PreprocessMessage](preprocessmessage.md)-Funktionsprototyp definierten Funktion geschrieben werden. Der MAPI-Spooler ruft in der Regel eine **RemovePreprocessInfo** -Funktion nach dem Senden einer Nachricht ab, die vorverarbeitete Informationen enthält. 
  

