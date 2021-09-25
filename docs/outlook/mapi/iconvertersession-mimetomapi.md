---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: a24c3cfacaf86369fd5229e9a8beb3dec13d589f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616845"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konvertiert einen MIME-Datenstrom in eine MAPI-Nachricht.
  
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
  
> [in] [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) zu einem MIME-Stream. 
    
 _pmsg_
  
> [in] Zeiger auf die zu ladende Nachricht. Der Aufrufer muss eine Nachricht bereitstellen, damit die API diese ausfüllt, sodass das Objekt [in] gehen muss. Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.
    
 _pszSrcSrv_
  
> [in] Dieser Wert muss **NULL** sein.
    
 _ulFlags_
  
> [in] Dieser Parameter identifiziert jede spezielle Aktion, die während der Konvertierung ausgeführt werden soll. Es muss null (0) sein, wenn keine bestimmte Aktion ausgeführt werden soll, oder eine Kombination der folgenden Werte:
    
CCSF_EMBEDDED_MESSAGE
  
> Gesendete/nicht gesendete Informationen werden in X-Unsent gespeichert.
    
CCSF_SMTP
  
> Der MIME-Stream ist für eine SMTP-Nachricht (Simple Mail Transfer Protocol) vorgesehen.
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger des MIME-Stroms sollten in die MAPI-Nachricht eingeschlossen werden.
    
CCSF_USE_RTF
  
> Der HTML-Text des MIME-Streams sollte in der MAPI-Nachricht in rtf (Rich Text Format) konvertiert werden.

CCSF_GLOBAL_MESSAGE
> Der Konverter sollte den MIME-Datenstrom als internationale Nachricht (EAI/RFC6530) verarbeiten. Wird unter Outlook 2013 nicht unterstützt.
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Gibt an, dass  _pstm_ **null** ist,  _pmsg_ **null** oder  _ulFlags_ ungültig ist. 
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie **CCSF_USE_RTF** als Teil von  _ulFlags_ angegeben haben und der Zielnachrichtenspeicher SOWOHL HTML als auch RTF unterstützt, wird die MAPI-Nachricht entweder in HTML oder RTF konvertiert. Wenn die Nachricht in RTF konvertiert wird, wird das konvertierte Format RTF komprimiert, alle HTML-Elemente werden in die komprimierte RTF-Zeichenfolge eingebettet, und die Zeichenfolge wird in der [kanonischen PidTagRtfCompressed-Eigenschaft](pidtagrtfcompressed-canonical-property.md)enthalten sein.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI-Konstanten](mapi-constants.md)

