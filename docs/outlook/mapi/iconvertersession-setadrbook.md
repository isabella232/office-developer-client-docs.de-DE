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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326894"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-in-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameter

 _PAB_
  
> in Zeiger auf eine [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) -Schnittstelle, die in der MAPI-zu-MIME-Konvertierung verwendet werden soll. Legen Sie diesen Parameter auf **null** fest, wenn Sie das Adressbuch nicht mehr benötigen; Dadurch wird die Schnittstelle freigegeben und der Konverter wird so zurückgesetzt, dass kein Adressbuch verwendet wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Das Konvertieren einer MAPI-Nachricht in einen MIME-Stream erfordert im Allgemeinen keine Anmeldung an einem MAPI-Profil. Wenn Sie jedoch ein MAPI-Adressbuch für die Konvertierung angeben, müssen Sie sich an einem Profil anmelden, um das Adressbuch abzurufen.
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

