---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d427dbf998a04f36e384baa7f029baa755b5d73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556504"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert die Präprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht). 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den Bezeichner enthält, den die Präprozessorfunktion verarbeitet. Der  _lpMuid-Parameter_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp für die Nachrichten, auf die die Funktion ausgeführt wird, z. B. FAX, SMTP oder X500. Der  _lpszAdrType-Parameter_ kann NULL sein. 
    
 _lpszDLLName_
  
> [in] Ein Zeiger auf den Namen der Dynamic Link Library (DLL), die den Einstiegspunkt für die Präprozessorfunktion enthält.
    
 _lpszPreprocess_
  
> [in] Ein Zeiger auf den Namen der Präprozessorfunktion. Der  _lpszPreprocess-Parameter_ kann NULL sein. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Ein Zeiger auf den Namen der Funktion, die Präprozessorinformationen entfernt (eine Funktion, die dem [RemovePreprocessInfo-Prototyp](removepreprocessinfo.md) entspricht). Der  _LpszRemovePreprocessInfo-Parameter_ kann NULL sein. 
    
 _ulFlags_
  
> Reserviert; muss Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Präprozessorfunktion wurde erfolgreich registriert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::RegisterPreprocessor-Methode** wird nur für Transportanbieter-Supportobjekte implementiert. Transportanbieter rufen **RegisterPreprocessor** auf, um eine Präprozessorfunktion (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht) zu registrieren. Eine Präprozessorfunktion muss registriert werden, bevor der MAPI-Spooler sie aufrufen kann. 
  
Die Parameter  _lpszPreprocess_,  _lpszRemovePreprocessInfo_ und  _lpszDLLName_ sollten alle auf Zeichenfolgen verweisen, die in Verbindung mit Aufrufen der Win32 **GetProcAddress-Funktion** verwendet werden können, sodass der DLL-Einstiegspunkt des Präprozessors korrekt aufgerufen werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Aufrufe an Vorauftragsverarbeiter sind spezifisch für die Transportanbieterreihenfolge. Dies bedeutet, dass die Präprozessorfunktion für diese Nachricht nicht aufgerufen wird, wenn ein anderer Transportanbieter vor Ihrem Anbieter eine Nachricht verarbeiten kann. Die Präprozessorfunktion wird nur für Nachrichten aufgerufen, die Sie behandeln.
  
Sie können Präprozessorfunktionen schreiben, um einen bestimmten Bezeichner zu verarbeiten, der in einer [MAPIUID-Struktur](mapiuid.md) gespeichert ist, oder einen Adresstyp. Wenn Sie sowohl eine **MAPIUID-Struktur** im  _lpMuid-Parameter_ als auch einen Adresstyp im  _lpszAdrType-Parameter_ angeben, wird Ihre Funktion für Nachrichtenempfänger aufgerufen, die entweder dem **MAPIUID-** oder dem Adresstyp entsprechen. Wenn  _lpMuid_ NULL und  _lpszAdrType_ ungleich NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, die eine Adresse haben, die dem Typ entspricht, auf den  _lpszAdrType_ verweist. Wenn  _lpMuid_ nicht NULL und  _lpszAdrType_ NULL ist, wird Ihre Funktion für Empfänger aufgerufen, die **MAPIUID** entsprechen, unabhängig vom Adresstyp. Wenn beide NULL sind, wird Ihre Funktion für alle Empfänger der Nachricht aufgerufen.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

