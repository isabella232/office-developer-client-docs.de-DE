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
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567916"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Registriert einen Adressbuchhierarchie Präprozessor-Funktion (eine Funktion, die den [PreprocessMessage](preprocessmessage.md) Prototyp entspricht). 
  
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
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den Bezeichner enthält, den die Präprozessor-Funktion behandelt. Der Parameter _LpMuid_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp für die Nachrichten wirkt sich die Funktion auf, wie FAX, SMTP oder X500. Der Parameter _LpszAdrType_ kann NULL sein. 
    
 _lpszDLLName_
  
> [in] Ein Zeiger auf den Namen des Dynamic Link Library (DLL), die den Einstiegspunkt für die Präprozessor-Funktion enthält.
    
 _lpszPreprocess_
  
> [in] Ein Zeiger auf den Namen der Präprozessor-Funktion. Der Parameter _LpszPreprocess_ kann NULL sein. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Ein Zeiger auf den Namen der Funktion, die entfernt Präprozessor Informationen (eine Funktion, die den [RemovePreprocessInfo](removepreprocessinfo.md) Prototyp entspricht). Der Parameter _LpszRemovePreprocessInfo_ kann NULL sein. 
    
 _ulFlags_
  
> Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Präprozessor-Funktion wurde erfolgreich registriert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::RegisterPreprocessor** -Methode wird für nur Unterstützungsobjekte der Transport-Anbieter implementiert. Transportanbieter Aufrufen **RegisterPreprocessor** zum Registrieren einer Präprozessor-Funktion (eine Funktion, die den [PreprocessMessage](preprocessmessage.md) Prototyp entspricht). Eine Funktion Präprozessor muss registriert werden, bevor die MAPI-Warteschlange aufgerufen werden kann. 
  
Der Parameter _LpszPreprocess_, _LpszRemovePreprocessInfo_und _LpszDLLName_ sollten alle in Zeichenfolgen verweisen, die in Verbindung mit der Aufrufe der Win32 **GetProcAddress** -Funktion, die der Präprozessor DLL zulassen verwendet werden können Einstiegspunkt ordnungsgemäß aufgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Anrufe an Präprozessoren sind für Transport Reihenfolge der Anbieter spezifisch. Dies bedeutet, dass wenn eine andere Adressbuchhierarchie vor Ihrem Anbieter um eine Nachricht zu verarbeiten kann, Ihre Funktion Präprozessor für diese Nachricht nicht aufgerufen wird. Nur für Nachrichten, die Sie behandelt, wird Ihre Präprozessor Funktion aufgerufen werden.
  
Sie können Präprozessor Funktionen zur Verarbeitung von entweder eines bestimmten Bezeichners in eine [MAPIUID](mapiuid.md) Struktur oder einen Adresstyp gespeichert schreiben. Wenn Sie eine **MAPIUID** -Struktur in der _LpMuid_ -Parameter und einen Adresstyp im _LpszAdrType_ -Parameter angeben, wird die Funktion für Empfänger der Nachricht aufgerufen werden, die die **MAPIUID** oder den Adresstyp entsprechen. Wenn _LpMuid_ NULL ist, und _LpszAdrType_ ungleich NULL ist, wird Ihre Funktion nur für Empfänger aufgerufen, der Adresse, die den Typ auf den _LpszAdrType_entspricht. Wenn _LpMuid_ ungleich NULL ist, und _LpszAdrType_ NULL ist, wird Ihre Funktion für Empfänger aufgerufen werden, die mit **MAPIUID**, unabhängig von deren Adresstyp übereinstimmen. Wenn beide NULL sind, wird die Funktion für alle Empfänger der Nachricht aufgerufen.
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

