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
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792031"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Betrifft**: Outlook 
  
Konvertiert einen MIME-Datenstrom an einem MAPI-Nachricht.
  
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
  
> [in] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle in eine MIME-Stream. 
    
 _pmsg_
  
> [out] Zeiger auf die Meldung geladen werden. Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.
    
 _pszSrcSrv_
  
> [in] Dieser Wert muss **null**sein.
    
 _ulFlags_
  
> [in] Dieser Parameter identifiziert eine spezielle Aktion während der Konvertierung erfolgen soll. Es muss null (0), wenn keine bestimmte Aktion ausgeführt werden soll, oder eine Kombination der folgenden Werte sein:
    
CCSF_EMBEDDED_MESSAGE
  
> Informationen gesendet/nicht gesendet wird dauerhaft in X nicht gesendet.
    
CCSF_SMTP
  
> Der MIME-Stream ist für eine Nachricht Simple MAPI-Transfer Protocol (SMTP).
    
CCSF_INCLUDE_BCC
  
> BCC-Empfänger des MIME-Streams sollte in der MAPI-Nachricht enthalten sein.
    
CCSF_USE_RTF
  
> Der HTML-Textkörper des MIME-Streams sollte auf Rich Text Format (RTF) in der MAPI-Nachricht konvertiert werden.
    
## <a name="return-value"></a>R�ckgabewert

E_INVALIDARG
  
> Gibt an, dass _Pstm_ **null ist**, _Pmsg_ **null ist**oder _UlFlags_ ungültig ist. 
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie **CCSF_USE_RTF** als Teil des _UlFlags_ angegeben haben, und der Nachricht Zielspeicher HTML- und RTF unterstützt, wird die MAPI-Nachricht in HTML oder RTF konvertiert werden. Wenn die Nachricht in RTF konvertiert wird, wird das Format der konvertierte komprimiert RTF, HTML-Code wird in der komprimierten RTF-Zeichenfolge eingebettet werden, und die Zeichenfolge wird in der [PidTagRtfCompressed kanonische-Eigenschaft](pidtagrtfcompressed-canonical-property.md)enthalten sein.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[MAPI-Konstanten](mapi-constants.md)

