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
  
Entfernt vorverarbeitete Informationen, die von einer [PreprocessMessage-basierten](preprocessmessage.md) Funktion geschrieben wurden, aus einer Nachricht. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI-Spooler  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Zeiger auf die vorverarbeitete Nachricht, aus der Informationen entfernt werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Vorverarbeitete Informationen wurden erfolgreich entfernt.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft eine Funktion basierend auf **RemovePreprocessInfo auf.** Ein Transportanbieter registriert die **RemovePreprocessInfo-basierte** Funktion gleichzeitig, wenn er die parallele **PreprocessMessage-basierte** Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode](imapisupport-registerpreprocessor.md) registriert. 
  
Ein Bildrendering, das für die Faxübertragung geeignet ist, ist ein Beispiel für vorverarbeitete Informationen, die von einer Funktion geschrieben wurden, die durch den Prototyp der [PreprocessMessage-Funktion](preprocessmessage.md)definiert wurde. Der MAPI-Spooler ruft in der Regel eine **RemovePreprocessInfo-Funktion** auf, nachdem eine Nachricht mit vorverarbeiteten Informationen gesendet wurde. 
  

