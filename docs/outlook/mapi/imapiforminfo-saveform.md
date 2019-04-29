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
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428746"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameter

 _szFileName_
  
> in Eine Zeichenfolge, die die Beschreibungsdatei des Formulars benennt, in der die Beschreibung gespeichert wird. Dieser Dateiname muss die. FDM-Erweiterung aufweisen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Die Konfigurationsdatei konnte nicht geschrieben werden. Rufen Sie die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode auf, um die [MAPIERROR](mapierror.md) -Struktur abzurufen, die dem Fehler zugeordnet ist. 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im lokalen Formular Container zu speichern. **SaveForm** wird für den lokalen Formular Container nicht unterstützt. 
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **IMAPIFormInfo:: SaveForm** -Methode auf, um eine Beschreibung des aktuellen Formulars in der Datei mit dem angegebenen Dateinamen zu speichern. **SaveForm** erstellt eine Konfigurationsdatei. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können Formulare neu installieren, indem Sie Sie in einer Liste von Formular Deskriptor-Nachrichten in einem Dialogfeld auswählen, das von Formularbibliothek Anbietern angezeigt wird. Die empfohlene Erweiterung für Formular Deskriptor-Nachrichten ist. fdm.
  
Rufen Sie die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode, wenn **SaveForm** MAPI_E_EXTENDED_ERROR zurückgibt, und überprüfen Sie die zurückgegebene **MAPIERROR** -Struktur, um die Bedingung zu bestimmen, die den Fehler verursacht hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

