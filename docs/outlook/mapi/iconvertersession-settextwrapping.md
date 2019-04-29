---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423587"
---
# <a name="iconvertersessionsettextwrapping"></a>IConverterSession::SetTextWrapping

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Breite des Textumbruchs für einen MIME-Stream fest, den der Konverter in [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md)zurückgibt.
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a>Parameter

 *fWrapText* 
  
> in Ob Text umbrochen werden soll oder nicht.
    
 *ulWrapWidth* 
  
> in Die zu verwendende Textumbruch Breite.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Anruf wurde erfolgreich ausgeführt.
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)


[MAPI-Konstanten](mapi-constants.md)

