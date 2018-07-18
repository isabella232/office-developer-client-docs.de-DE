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
ms.openlocfilehash: e6880a32e30b8f208ce5ba0a2d30e635ff464461
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792033"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Betrifft**: Outlook 
  
Gibt ein optionales MAPI-Adressbuch, die MAPI zu MIME-Konverter verwendet, um mehrdeutige Adressen aufzulösen, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameter

 _PAB_
  
> [in] Zeiger auf eine [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) Schnittstelle in der MAPI in MIME-Konvertierung verwendet werden. Legen Sie diesen Parameter auf **null festgelegt** , wenn Sie nicht mehr im Adressbuch benötigen; Dies gibt die Schnittstelle und setzt den Konverter auf beliebiges Adressbuch nicht verwenden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Funktionsaufruf ist erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Konvertieren von MAPI erforderlich keine Nachrichten in MIME-Stream-Objekt im Allgemeinen Protokollierung bei einem MAPI-Profil. Angeben von einem MAPI-Adressbuch für die Konvertierung erfordert jedoch zu einem Profil Abrufen des Adressbuchs anmelden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI (engl.) wandelt MimeToMAPI eine EML-Datei an einen MAPI-Nachricht.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI (engl.) wird MAPIToMIMEStm verwendet, um eine MAPI-Nachricht in einer EML-Datei zu konvertieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

