---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326929"
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
  
> Out Zeiger auf die zu ladende Nachricht. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMESSAGE**.
    
 _pszSrcSrv_
  
> in Dieser Wert muss **null**sein.
    
 _ulFlags_
  
> in Dieser Parameter identifiziert eine besondere Aktion, die während der Konvertierung durchgeführt werden soll. Es muss NULL (0) sein, wenn keine bestimmte Aktion ausgeführt werden soll, oder eine Kombination der folgenden Werte:
    
CCSF_EMBEDDED_MESSAGE
  
> Gesendete/nicht gesendete Informationen werden in X-unsent gespeichert.
    
CCSF_SMTP
  
> Der MIME-Stream ist für eine SMTP-Nachricht (Simple MAPI Transfer Protocol).
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger des MIME-Streams sollten in der MAPI-Nachricht enthalten sein.
    
CCSF_USE_RTF
  
> Der HTML-Textkörper des MIME-Streams sollte in Rich-Text-Format (RTF) in der MAPI-Nachricht konvertiert werden.

CCSF_GLOBAL_MESSAGE
> Der Konverter sollte den MIME-Stream als internationale Nachricht behandeln (EAI/RFC6530). In Outlook 2013 nicht unterstützt.
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Gibt an, dass _pstm_ den Wert **null**hat, _Pmsg_ ist **null**, oder _ulFlags_ ist ungültig. 
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie **CCSF_USE_RTF** als Teil von _ulFlags_ angegeben haben und der Ziel Nachrichtenspeicher sowohl HTML als auch RTF unterstützt, wird die MAPI-Nachricht in HTML oder RTF konvertiert. Wenn die Nachricht in RTF konvertiert wird, wird das konvertierte Format RTF komprimiert, jeder HTML-Code wird in die komprimierte RTF-Zeichenfolge eingebettet, und die Zeichenfolge wird in der [kanonischEn Eigenschaft PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)enthalten sein.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI-Konstanten](mapi-constants.md)

