---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 563f83d6ebb76659afa99e446378b8d68a8e80b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613947"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Zeiger auf die zu konvertierende Nachricht. Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.
    
 _pstm_
  
> [out] [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) zum Ausgeben des Datenstroms. 
    
 _ulFlags_
  
>  [in] Flags, die bestimmte Aktionen für den Konverter angeben: 
    
CCSF_8BITHEADERS
  
> Der Konverter sollte 8-Bit-Header zulassen.
    
CCSF_EMBEDDED_MESSAGE
  
> Gesendete/nicht gesendete Informationen werden in X-Unsent gespeichert.
    
CCSF_GLOBAL_MESSAGE
  
> Der Konverter sollte eine internationale Nachricht (EAI/RFC6530) erstellen.
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger der MAPI-Nachricht sollten in den MIME-Stream eingeschlossen werden.
    
CCSF_NO_MSGID
  
> Schließen Sie Message-Id Feld nicht in ausgehende Nachrichten ein.
    
CCSF_NOHEADERS
  
> Der Konverter sollte die Kopfzeilen der externen Nachricht ignorieren.
    
CCSF_PLAIN_TEXT_ONLY
  
> Der Konverter sollte nur Nur-Text senden.
    
CCSF_SMTP
  
> Dem Konverter wird eine SMTP-Nachricht übergeben. Dieses Kennzeichen muss immer festgelegt werden.
    
CCSF_USE_RTF
  
> Der Konverter sollte in der MIME-Nachricht vom HTML- in das RTF-Format konvertiert werden.
    
CCSF_USE_TNEF
  
> Der Konverter sollte das TNEF-Format (Transport Neutral Encapsulation Format) in der MIME-Nachricht verwenden.
    
## <a name="return-values"></a>Rückgabewerte

E_INVALIDARG
  
> Ungültige Flags wurden übergeben, oder  *pmsg*  oder  *pstm*  ist NULL. 
    
## <a name="remarks"></a>Bemerkungen

Wird nur für Standardnachrichtentypen Outlook unterstützt.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[PidTagMessageEditorFormat (kanonische Eigenschaft)](pidtagmessageeditorformat-canonical-property.md)
  
[Kanonische PidLidUseTnef-Eigenschaft](pidlidusetnef-canonical-property.md)


[MAPI-Konstanten](mapi-constants.md)

