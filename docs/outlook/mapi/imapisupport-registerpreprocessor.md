---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404897"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert die präprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage](preprocessmessage.md) -Prototyp entspricht). 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpMuid_
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Bezeichner enthält, den die präprozessorfunktion verarbeitet. Der _lpMuid_ -Parameter kann NULL sein. 
    
 _lpszAdrType_
  
> in Ein Zeiger auf den Adresstyp für die Nachrichten, auf denen die Funktion ausgeführt wird, wie FAX, SMTP oder x500. Der _lpszAdrType_ -Parameter kann NULL sein. 
    
 _lpszDLLName_
  
> in Ein Zeiger auf den Namen der Dynamic Link Library (DLL), die den Einstiegspunkt für die präprozessorfunktion enthält.
    
 _lpszPreprocess_
  
> in Ein Zeiger auf den Namen der präprozessorfunktion. Der _lpszPreprocess_ -Parameter kann NULL sein. 
    
 _lpszRemovePreprocessInfo_
  
> in Ein Zeiger auf den Namen der Funktion, die präprozessorinformationen (eine Funktion, die dem [RemovePreprocessInfo](removepreprocessinfo.md) -Prototyp entspricht) entfernt. Der _lpszRemovePreprocessInfo_ -Parameter kann NULL sein. 
    
 _ulFlags_
  
> Reserviert muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die präprozessorfunktion wurde erfolgreich registriert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: RegisterPreprocessor** -Methode wird nur für Transportanbieter-Support Objekte implementiert. Transport Anbieter rufen **RegisterPreprocessor** auf, um eine präprozessorfunktion (eine Funktion, die dem [PreprocessMessage](preprocessmessage.md) -Prototyp entspricht) zu registrieren. Eine präprozessorfunktion muss registriert werden, bevor Sie vom MAPI-Spooler aufgerufen werden kann. 
  
Die _lpszPreprocess_-, _LpszRemovePreprocessInfo_-und _lpszDLLName_ -Parameter sollten alle auf Zeichenfolgen verweisen, die in Verbindung mit Aufrufen der Win32- **GetProcAddress** -Funktion verwendet werden können, sodass die DLL des Präprozessors der Einstiegspunkt, der richtig aufgerufen werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Aufrufe an Präprozessoren sind spezifisch für die Transportanbieter Reihenfolge. Dies bedeutet, dass die präprozessorfunktion für diese Nachricht nicht aufgerufen wird, wenn ein anderer Transportanbieter vor dem Anbieter eine Nachricht verarbeiten kann. Ihre präprozessorfunktion wird nur für Nachrichten aufgerufen, die Sie behandeln.
  
Sie können präprozessorfunktionen schreiben, um einen bestimmten Bezeichner zu behandeln, der in einer [MAPIUID](mapiuid.md) -Struktur oder einem Adresstyp gespeichert ist. Wenn Sie sowohl eine **MAPIUID** -Struktur im _lpMuid_ -Parameter als auch einen Adresstyp im _lpszAdrType_ -Parameter angeben, wird Ihre Funktion für Nachrichtenempfänger aufgerufen, die mit dem **MAPIUID** oder dem Adresstyp übereinstimmen. Wenn _lpMuid_ ist und _LPSZADRTYPE_ ungleich NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, die über eine Adresse verfügen, die mit dem Typ übereinstimmt, auf den von _lpszAdrType_verwiesen wird. Wenn _lpMuid_ nicht NULL ist und _LPSZADRTYPE_ den Wert NULL hat, wird Ihre Funktion für Empfänger aufgerufen, die **MAPIUID**entsprechen, unabhängig von Ihrem Adresstyp. Wenn beide NULL sind, wird Ihre Funktion für alle Empfänger der Nachricht aufgerufen.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

