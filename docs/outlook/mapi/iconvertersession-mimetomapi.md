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
description: 'Letzte Änderung: 06. September 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160286"
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
  
> [in] [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) zu einem MIME-Stream. 
    
 _pmsg_
  
> [in] Zeiger auf die zu ladende Nachricht. Der Aufrufer muss eine Meldung zum Ausfüllen der API liefern, damit das Objekt [in] wechseln muss. Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.
    
 _pszSrcSrv_
  
> [in] Dieser Wert muss **null sein.**
    
 _ulFlags_
  
> [in] Dieser Parameter identifiziert alle besonderen Aktionen, die während der Konvertierung ergriffen werden müssen. Es muss null (0) sein, wenn keine bestimmte Aktion oder eine Kombination der folgenden Werte ergriffen werden soll:
    
CCSF_EMBEDDED_MESSAGE
  
> Gesendete/nicht gesendete Informationen werden in X-Unsent beibehalten.
    
CCSF_SMTP
  
> Der MIME-Stream ist für eine SIMPLE Mail Transfer Protocol (SMTP)-Nachricht.
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger des MIME-Datenstroms sollten in der MAPI-Nachricht enthalten sein.
    
CCSF_USE_RTF
  
> Der HTML-Textkörper des MIME-Datenstroms sollte in der MAPI-Nachricht in das Rich Text Format (RTF) konvertiert werden.

CCSF_GLOBAL_MESSAGE
> Der Konverter sollte den MIME-Stream als internationale Nachricht behandeln (EAI/RFC6530). Wird in Outlook 2013 nicht unterstützt.
    
## <a name="return-value"></a>Rückgabewert

E_INVALIDARG
  
> Gibt an,  _dass pstm_ **null** ist,  _pmsg_ **null** oder  _ulFlags_ ungültig ist. 
    
## <a name="remarks"></a>Hinweise

Wenn Sie  CCSF_USE_RTF als Teil von _ulFlags_ angegeben haben und der Zielnachrichtenspeicher HTML und RTF unterstützt, wird die MAPI-Nachricht in HTML oder RTF konvertiert. Wenn die Nachricht in RTF konvertiert wird, wird das konvertierte Format rtF komprimiert, alle #A0 in die komprimierte #A1 eingebettet, und die Zeichenfolge ist in der [kanonischen Eigenschaft PidTagRtfCompressed enthalten.](pidtagrtfcompressed-canonical-property.md)
  
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

