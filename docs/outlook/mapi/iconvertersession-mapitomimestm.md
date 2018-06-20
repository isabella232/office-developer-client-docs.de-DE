---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Zuletzt geändert: 20 September 2017'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792030"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Betrifft**: Outlook 
  
Konvertiert eine MAPI-Nachricht in einen MIME-Stream.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameter

 _pmsg_
  
> [in] Zeiger auf die Nachricht zu konvertieren. Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.
    
 _pstm_
  
> [out] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle an den Stream ausgegeben. 
    
 _ulFlags_
  
>  [in] Flags, die für den Konverter bestimmte Aktionen angeben: 
    
CCSF_8BITHEADERS
  
> Der Konverter sollte 8-Bit-Kopfzeilen zulassen.
    
CCSF_EMBEDDED_MESSAGE
  
> Informationen gesendet/nicht gesendet wird dauerhaft in X nicht gesendet.
    
CCSF_GLOBAL_MESSAGE
  
> Der Konverter sollte eine internationale Nachricht (EAI/RFC6530) erstellt werden.
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger der Nachricht MAPI sollte im MIME-Datenstrom enthalten sein.
    
CCSF_NO_MSGID
  
> Nehmen Sie Nachrichten-Id-Feld nicht in ausgehenden Nachrichten aus.
    
CCSF_NOHEADERS
  
> Der Konverter sollten die Kopfzeilen der äußeren Nachricht ignorieren.
    
CCSF_PLAIN_TEXT_ONLY
  
> Der Konverter sollte nur nur-Text senden.
    
CCSF_SMTP
  
> Der Konverter ist eine SMTP-Nachricht übergeben wird. Dieses Kennzeichen müssen immer festgelegt werden.
    
CCSF_USE_RTF
  
> Der Konverter sollten aus HTML-Code der MIME-Nachricht im RTF-Format konvertieren.
    
CCSF_USE_TNEF
  
> Der Konverter sollten Transport Neutral Encapsulation Format (TNEF) Format der MIME-Nachricht verwenden.
    
## <a name="return-values"></a>Rückgabewerte

E_INVALIDARG
  
> Ungültige Flags übergeben wurden, oder *Pmsg* oder *Pstm* ist NULL. 
    
## <a name="remarks"></a>Hinweise

Nur für Outlook-Nachricht Standardtypen unterstützt.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession: IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Kanonische PidTagMessageEditorFormat-Eigenschaft](pidtagmessageeditorformat-canonical-property.md)
  
[Kanonische PidLidUseTnef-Eigenschaft](pidlidusetnef-canonical-property.md)


[MAPI-Konstanten](mapi-constants.md)

