---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429194"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein optionales MAPI-Adressbuch an, das der MAPI-zu-MIME-Konverter zum Auflösen mehrdeutiger Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameter

 _pab_
  
> [in] Zeiger auf ein [IAddrBook : IMAPIProp-Schnittstelle,](iaddrbookimapiprop.md) die in der MAPI-zu-MIME-Konvertierung verwendet werden soll. Legen Sie diesen Parameter **auf null,** wenn Sie das Adressbuch nicht mehr benötigen. Dadurch wird die Schnittstelle veröffentlicht, und der Konverter wird auf kein Adressbuch zurückgesetzt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="remarks"></a>Hinweise

Für das Konvertieren einer MAPI-Nachricht in einen MIME-Stream ist in der Regel keine Anmeldung bei einem MAPI-Profil erforderlich. Wenn Sie jedoch ein MAPI-Adressbuch für die Konvertierung angeben, müssen Sie sich bei einem Profil anmelden, um das Adressbuch zu erhalten.
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

