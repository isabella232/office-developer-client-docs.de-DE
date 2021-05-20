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
  
> [in] Eine Zeichenfolge, die die Beschreibungsnachrichtendatei des Formulars benennt, in der die Beschreibung gespeichert wird. Dieser Dateiname muss die .fdm-Erweiterung haben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Die Konfigurationsdatei konnte nicht geschrieben werden. Rufen Sie die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, um die [MAPIERROR-Struktur](mapierror.md) zu erhalten, die dem Fehler zugeordnet ist. 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** wurde wahrscheinlich aufgerufen, um ein Formular im lokalen Formularcontainer zu speichern. **SaveForm** wird im lokalen Formularcontainer nicht unterstützt. 
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **IMAPIFormInfo::SaveForm-Methode** auf, um eine Beschreibung des aktuellen Formulars in der Datei mit dem angegebenen Dateinamen zu speichern. **SaveForm** erstellt eine Konfigurationsdatei. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können Formulare erneut installieren, indem Sie sie aus einer Liste von Formularbeschreibungsmeldungen in einem Dialogfeld auswählen, das von Formularbibliotheksanbietern angezeigt wird. Die empfohlene Erweiterung für Formulardeskriptormeldungen ist .fdm.
  
Rufen Sie [die IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) auf, wenn **SaveForm** MAPI_E_EXTENDED_ERROR zurückgibt, und überprüfen Sie die zurückgegebene **MAPIERROR-Struktur,** um die Bedingung zu ermitteln, die den Fehler verursacht hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

