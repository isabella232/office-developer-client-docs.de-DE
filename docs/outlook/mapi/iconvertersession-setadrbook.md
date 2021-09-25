---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d05b08cd18b075119017163c7142e88afba82121
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600985"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-zu-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameter

 _Pab_
  
> [in] Zeiger auf ein [IAddrBook: IMAPIProp-Schnittstelle,](iaddrbookimapiprop.md) die in der MAPI-zu-MIME-Konvertierung verwendet werden soll. Legen Sie diesen Parameter auf **NULL** fest, wenn Sie das Adressbuch nicht mehr benötigen. Dadurch wird die Schnittstelle los, und der Konverter wird auf kein Adressbuch zurückgesetzt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Für das Konvertieren einer MAPI-Nachricht in einen MIME-Stream ist in der Regel keine Anmeldung bei einem MAPI-Profil erforderlich. Wenn Sie jedoch ein MAPI-Adressbuch für die Konvertierung angeben, müssen Sie sich bei einem Profil anmelden, um das Adressbuch abzurufen.
  
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

