---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 827f13571babdebf4fca8255575e811fda9992db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599137"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt vorverarbeitete Informationen, die von einer [PreprocessMessage-basierten](preprocessmessage.md) Funktion geschrieben wurden, aus einer Nachricht. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI-Spooler  <br/> |
   
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft eine Funktion auf der Grundlage **von RemovePreprocessInfo** auf. Ein Transportanbieter registriert die **RemovePreprocessInfo-basierte** Funktion gleichzeitig und registriert die parallele **preprocessMessage-basierte** Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode.](imapisupport-registerpreprocessor.md) 
  
Ein für die Faxübertragung geeignetes Bildrendering ist ein Beispiel für vorverarbeitete Informationen, die von einer funktion geschrieben wurden, die durch den Prototyp der [PreprocessMessage-Funktion](preprocessmessage.md)definiert wurde. Der MAPI-Spooler ruft in der Regel eine **RemovePreprocessInfo-Funktion** auf, nachdem eine Nachricht gesendet wurde, die vorverarbeitete Informationen enthält. 
  

