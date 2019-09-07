---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Letzte Änderung: September 06, 2019'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790771"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert einen MIME-Stream in eine MAPI-Nachricht.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameter

 _pstm_
  
> in [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle zu einem MIME-Stream. 
    
 _pmsg_
  
> in Zeiger auf die zu ladende Nachricht. Der Aufrufer muss eine Nachricht angeben, damit die API ausgefüllt wird, damit das Objekt [in] gehen muss. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMESSAGE**.
    
 _pszSrcSrv_
  
> in Dieser Wert muss **null**sein.
    
 _ulFlags_
  
> in Dieser Parameter gibt alle speziellen Aktionen an, die während der Konvertierung durchgeführt werden sollen. Es muss NULL (0) sein, wenn keine bestimmte Aktion ausgeführt werden soll, oder eine Kombination der folgenden Werte:
    
CCSF_EMBEDDED_MESSAGE
  
> Gesendete/nicht gesendete Informationen werden in X-unsent gespeichert.
    
CCSF_SMTP
  
> Der MIME-Datenstrom ist für eine SMTP-Nachricht (Simple MAPI Transfer Protocol).
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger des MIME-Streams sollten in die MAPI-Nachricht aufgenommen werden.
    
CCSF_USE_RTF
  
> Der HTML-Text des MIME-Streams sollte in die MAPI-Nachricht in Rich-Text-Format (RTF) konvertiert werden.

CCSF_GLOBAL_MESSAGE
> Der Konverter sollte den MIME-Datenstrom als internationale Nachricht behandeln (EAI/RFC6530). Für Outlook 2013 nicht unterstützt.
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Gibt an, dass _pstm_ **null**ist, _pmsg_ ist **null**, oder _ulFlags_ ist ungültig. 
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie **CCSF_USE_RTF** als Teil von _ulFlags_ angegeben haben und der Ziel Nachrichtenspeicher sowohl HTML als auch RTF unterstützt, wird die MAPI-Nachricht entweder in HTML oder in RTF konvertiert. Wenn die Nachricht in RTF konvertiert wird, wird das konvertierte Format in RTF komprimiert, alle HTML-Elemente werden in die komprimierte RTF-Zeichenfolge eingebettet, und die Zeichenfolge wird in der [kanonischen PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md)enthalten sein.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MfcMapi verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MfcMapi verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI-Konstanten](mapi-constants.md)

