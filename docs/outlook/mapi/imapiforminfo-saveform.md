---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593473"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameter

 _szFileName_
  
> [in] Eine Zeichenfolge, die das Formular Nachricht Beschreibungsdatei benennt, in dem die Beschreibung gespeichert ist. Gibt den Dateinamen muss die .fdm-Erweiterung aufweisen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Die Konfigurationsdatei konnte nicht geschrieben werden. Um die Struktur [MAPIERROR](mapierror.md) abzurufen, die dem Fehler zugeordnet ist, rufen Sie die [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode. 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im Container lokale Formular zu speichern. **SaveForm** wird für den Container lokale Formular nicht unterstützt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen Sie die **IMAPIFormInfo::SaveForm** -Methode, um eine Beschreibung des aktuellen Formulars in der Datei zu speichern, die den angegebenen Dateinamen hat. **SaveForm** erstellt eine Konfigurationsdatei. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können Formulare, indem Sie sie aus einer Liste von Formular Deskriptor Nachrichten in einem Dialogfeld, die Bibliothek Anbieter Anzeige bilden auswählen installieren. Die empfohlene Erweiterung für das Formular Deskriptor Nachrichten ist .fdm.
  
Rufen Sie die Methode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) **SaveForm** MAPI_E_EXTENDED_ERROR zurück, und überprüfen Sie die zurückgegebene **MAPIERROR** -Struktur, um die Bedingung zu ermitteln, die den Fehler verursacht hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

