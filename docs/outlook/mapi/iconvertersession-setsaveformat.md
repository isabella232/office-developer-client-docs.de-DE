---
title: IConverterSessionSetSaveFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f24ad938fdb8c3ac234e1d78f2668139840c8b8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568217"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Legt das Format, in dem der Konverter MIME-Stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)zurück.
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>Parameter

_mstSaveFormat_
  
> [in] Das Speichern-format für einen MIME-Stream verwendet werden soll. Weitere Informationen finden Sie unter den Enumerationstyp [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).
    
  - **SAVE_RFC1521**: Verwendung MIME, was die Standardeinstellung ist.      
  - **SAVE_RFC822**: Uuencode verwenden.
    
## <a name="return-values"></a>Rückgabewerte

S_OK
  
> Der Aufruf war erfolgreich.
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [MAPI-Konstanten](mapi-constants.md)

