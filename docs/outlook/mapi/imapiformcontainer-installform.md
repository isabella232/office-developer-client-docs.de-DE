---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d329d3a14b6026d0bd62df9feba6ccff251e4151
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792147"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Betrifft**: Outlook 
  
Wird ein Formular in einer Formularbibliothek installiert.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, die Clientanwendung das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt. Der Parameter _UlUIParam_ kann NULL sein, wenn MAPI_DIALOG nicht auch übergeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Installation des Formulars steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld zum Bereitstellen von Fortschrittsinformationen oder auffordern, Weitere Informationen an. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Wenn ein anderes Formular bereits vorhanden, behandelt dieses Formular die Nachrichtenklasse behandelt ist, ersetzen Sie das bestehende Formular mit diesem. Dieses Kennzeichen werden ignoriert, wenn das Flag MAPI_DIALOG auch vorhanden ist. 
    
 _szCfgPathName_
  
> [in] Der Pfad zur Konfigurationsdatei für das Formular.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein Implementierung Fehler aufgetreten. Um die Struktur [MAPIERROR](mapierror.md) abzurufen, die dem Fehler zugeordnet ist, rufen Sie die [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) -Methode. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat die Installation des Formulars, in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formular Bibliothek Anbieter sollte eine **MAPIERROR** Struktur füllen und MAPI_E_EXTENDED_ERROR zurück, wenn Sie eine der folgenden Situationen auftreten: 
  
- Die Konfigurationsdatei wurde nicht gefunden.
    
- Die Konfigurationsdatei kann nicht gelesen werden.
    
- Die Konfigurationsdatei ist ungültig.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen rufen Sie die **IMAPIFormContainer::InstallForm** -Methode, um ein Formular in ein bestimmtes Formular Container zu installieren. Der Parameter _SzCfgPathName_ muss den Pfad einer Konfigurationsdatei Formular (d. h., eine Datei mit der cfg-Erweiterung, die das Formular und deren Implementierung beschreibt) enthalten. Die Kennzeichen im Parameter _UlFlags_ geben Folgendes an: 
  
- Wenn das Flag MAPI_DIALOG festgelegt ist, wird eine Benutzeroberfläche angezeigt, durch den Benutzer, der das Formular, um die Installationsdetails angeben installiert.
    
- Wenn das Flag MAPIFORM_INSTALL_OVERWRITEONCONFLICT festgelegt ist, wird mit dem Formular installiert alle vorherigen Formular für dieselbe Nachrichtenklasse ersetzt. Andernfalls wird die Installation des Formulars mit der aktuellen formularbeschreibung zusammengeführt, sofern vorhanden.
    
- Wenn MAPI_DIALOG festgelegt ist, wird die MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.
    
- Das fehlen MAPIFORM_INSTALL_OVERWRITEONCONFLICT in das Flag festlegen bedeutet, die eine Zusammenführung durchgeführt wird. Neuen Plattformen in die cfg-Datei, die nicht in der formularbeschreibung derzeit vorhanden sind installiert werden und keine anderen Änderungen erfolgt.
    
- Wenn die Option MAPI_UNICODE festgelegt ist, ist der Pfad der Konfigurationsdatei Formular eine Unicode-Zeichenfolge. 
    
Clients sollte [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) aufrufen, wenn **InstallForm** MAPI_E_EXTENDED_ERROR zurückgegeben, und sie, dass die zurückgegebene [MAPIERROR](mapierror.md) -Struktur überprüfen sollten, um die Bedingung zu ermitteln, die den Fehler ausgelöst hat. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormContainer::InstallForm** -Methode, um ein Formular in einem Formular Container installieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

