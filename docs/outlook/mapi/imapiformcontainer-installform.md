---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f8f5db6ebb264788de6a9c8a570056c3d8ace8e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621003"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Installiert ein Formular in einer Formularbibliothek.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, die Clientanwendung legt das flag MAPI_DIALOG im  _ulFlags-Parameter_ fest. Der  _ulUIParam-Parameter_ kann NULL sein, wenn MAPI_DIALOG nicht auch übergeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Installation des Formulars steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld zum Bereitstellen von Statusinformationen an oder fordert den Benutzer auf, weitere Informationen einzufordern. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Wenn bereits ein anderes Formular vorhanden ist, das die von diesem Formular verarbeitete Nachrichtenklasse verarbeitet, ersetzen Sie das vorhandene Formular durch dieses Formular. Dieses Flag wird ignoriert, wenn das MAPI_DIALOG Flag ebenfalls vorhanden ist. 
    
 _szCfgPathName_
  
> [in] Der Pfad zur Konfigurationsdatei des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Es ist ein Implementierungsfehler aufgetreten. Rufen Sie zum Abrufen der [MAPIERROR-Struktur,](mapierror.md) die dem Fehler zugeordnet ist, die [IMAPIFormContainer::GetLastError-Methode](imapiformcontainer-getlasterror.md) auf. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat die Installation des Formulars abgebrochen, in der Regel durch Klicken auf die Schaltfläche **"Abbrechen"** in einem Dialogfeld. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formularbibliotheksanbieter sollten eine **MAPIERROR-Struktur** ausfüllen und MAPI_E_EXTENDED_ERROR zurückgeben, wenn eine der folgenden Bedingungen auftritt: 
  
- Die Konfigurationsdatei wurde nicht gefunden.
    
- Die Konfigurationsdatei ist nicht lesbar.
    
- Die Konfigurationsdatei ist ungültig.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen rufen die **IMAPIFormContainer::InstallForm-Methode** auf, um ein Formular in einem bestimmten Formularcontainer zu installieren. Der  _parameter szCfgPathName_ muss den Pfad einer Formularkonfigurationsdatei enthalten (d. h. eine Datei mit der Erweiterung CFG, die das Formular und dessen Implementierung beschreibt). Die Flags im  _ulFlags-Parameter_ geben Folgendes an: 
  
- Wenn das flag MAPI_DIALOG festgelegt ist, wird eine Benutzeroberfläche angezeigt, über die der Benutzer, der das Formular installiert, Installationsdetails angeben kann.
    
- Wenn das flag MAPIFORM_INSTALL_OVERWRITEONCONFLICT festgelegt ist, wird jedes vorherige Formular für dieselbe Nachrichtenklasse durch das zu installierende Formular ersetzt. Andernfalls wird die Formularinstallation mit der aktuellen Formularbeschreibung zusammengeführt, sofern vorhanden.
    
- Wenn MAPI_DIALOG festgelegt ist, wird MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.
    
- Das Fehlen von MAPIFORM_INSTALL_OVERWRITEONCONFLICT im Flagsatz bedeutet, dass eine Zusammenführung durchgeführt wird. Alle neuen Plattformen in der CFG-Datei, die derzeit nicht in der Formularbeschreibung vorhanden sind, werden installiert, und es werden keine weiteren Änderungen vorgenommen.
    
- Wenn das flag MAPI_UNICODE festgelegt ist, ist der Pfad der Formularkonfigurationsdatei eine Unicode-Zeichenfolge. 
    
Clients sollten [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) aufrufen, wenn **InstallForm** MAPI_E_EXTENDED_ERROR zurückgibt, und sie sollten die zurückgegebene [MAPIERROR-Struktur](mapierror.md) überprüfen, um die Bedingung zu ermitteln, die den Fehler ausgelöst hat. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::InstallForm-Methode,** um ein Formular in einem Formularcontainer zu installieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

