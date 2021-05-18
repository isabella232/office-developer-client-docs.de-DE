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
  
Registriert die Preprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht). 
  
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
  
> [in] Ein Zeiger auf den Adresstyp für die Nachrichten, für die die Funktion arbeitet, z. B. FAX, SMTP oder X500. Der  _lpszAdrType-Parameter_ kann NULL sein. 
    
 _lpszDLLName_
  
> [in] Ein Zeiger auf den Namen der Dynamic-Link Library (DLL), die den Einstiegspunkt für die Präprozessorfunktion enthält.
    
 _lpszPreprocess_
  
> [in] Ein Zeiger auf den Namen der Präprozessorfunktion. Der  _lpszPreprocess-Parameter_ kann NULL sein. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Ein Zeiger auf den Namen der Funktion, die Vorverarbeitungsinformationen entfernt (eine Funktion, die dem [RemovePreprocessInfo-Prototyp entspricht).](removepreprocessinfo.md) Der  _lpszRemovePreprocessInfo-Parameter_ kann NULL sein. 
    
 _ulFlags_
  
> Reserviert; muss null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Preprocessor-Funktion wurde erfolgreich registriert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::RegisterPreprocessor-Methode** wird nur für Unterstützungsobjekte des Transportanbieters implementiert. Transportanbieter rufen **RegisterPreprocessor auf,** um eine Präprozessorfunktion zu registrieren (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht). Eine Präprozessorfunktion muss registriert werden, bevor der MAPI-Spooler sie aufrufen kann. 
  
Die  _Parameter lpszPreprocess,_  _lpszRemovePreprocessInfo_ und  _lpszDLLName_ sollten alle auf Zeichenfolgen verweisen, die zusammen mit Aufrufen der Win32 **GetProcAddress-Funktion** verwendet werden können, sodass der DLL-Einstiegspunkt des Präprozessors ordnungsgemäß aufgerufen werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Aufrufe an Präprozessoren sind spezifisch für die Reihenfolge des Transportanbieters. Dies bedeutet, dass, wenn ein anderer Transportanbieter vor Ihrem Anbieter eine Nachricht verarbeiten kann, Ihre Präprozessorfunktion nicht für diese Nachricht aufgerufen wird. Ihre Präprozessorfunktion wird nur für Nachrichten aufgerufen, die Sie behandeln.
  
Sie können Präprozessorfunktionen schreiben, um entweder einen bestimmten Bezeichner zu verarbeiten, der in einer [MAPIUID-Struktur](mapiuid.md) gespeichert ist, oder einen Adresstyp. Wenn Sie sowohl eine **MAPIUID-Struktur** im  _lpMuid-Parameter_ als auch einen Adresstyp im  _lpszAdrType-Parameter_ angeben, wird Ihre Funktion für Nachrichtenempfänger aufgerufen, die entweder der **MAPIUID** oder dem Adresstyp entsprechen. Wenn _lpMuid_ NULL und _lpszAdrType_ nicht NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, die eine Adresse haben, die dem Typ entspricht, auf den _lpszAdrType verweist._ Wenn  _lpMuid_ nicht NULL und  _lpszAdrType_ NULL ist, wird Ihre Funktion für Empfänger aufgerufen, die **MAPIUID** entsprechen, unabhängig vom Adresstyp. Wenn beide Null sind, wird Ihre Funktion für alle Empfänger der Nachricht aufgerufen.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

