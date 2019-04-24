---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321546"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert die aktuelle Nachricht in einen Ordner.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parameter

 _pFolderDestination_
  
> in Ein Zeiger auf den Ordner, in den die Nachricht kopiert werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite:: CopyMessage** -Methode auf, um die aktuelle Nachricht in einen neuen Ordner zu kopieren. **CopyMessage** ändert die aktuell angezeigte Nachricht nicht, und es wird keine Schnittstelle für die neu erstellte Nachricht an das Formular zurückgegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine typische Implementierung der **CopyMessage** -Methode führt die folgenden Aufgaben aus: 
  
1. Erstellt eine neue Nachricht für die aktuelle Nachricht, in die kopiert werden soll.
    
2. Ruft die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode mit einem Zeiger auf die neue Nachricht im _pMessage_ -Parameter und false im _fSameAsLoad_ -Parameter auf. 
    
3. Ruft die [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) -Methode auf und übergibt NULL im _pMessage_ -Parameter. 
    
4. Ruft die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die neue Nachricht auf. 
    
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: CopyMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

