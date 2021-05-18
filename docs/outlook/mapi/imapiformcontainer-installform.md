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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405086"
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
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, die Clientanwendung legt das MAPI_DIALOG im  _ulFlags-Parameter_ fest. Der  _ulUIParam-Parameter_ kann NULL sein, MAPI_DIALOG nicht auch übergeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Installation des Formulars steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, um Statusinformationen zur Verfügung zu stellen oder den Benutzer zu weiteren Informationen aufforderen. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Wenn bereits ein anderes Formular vorhanden ist, das die von diesem Formular behandelte Nachrichtenklasse behandelt, ersetzen Sie das vorhandene Formular durch dieses Formular. Dieses Flag wird ignoriert, wenn MAPI_DIALOG auch vorhanden ist. 
    
 _szCfgPathName_
  
> [in] Der Pfad zur Konfigurationsdatei des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein Implementierungsfehler ist aufgetreten. Rufen Sie die [IMAPIFormContainer::GetLastError-Methode](imapiformcontainer-getlasterror.md) auf, um die [MAPIERROR-Struktur](mapierror.md) zu erhalten, die dem Fehler zugeordnet ist. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat die Installation des Formulars abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Formularbibliotheksanbieter sollten eine **MAPIERROR-Struktur** ausfüllen und MAPI_E_EXTENDED_ERROR, wenn eine der folgenden Bedingungen auftritt: 
  
- Die Konfigurationsdatei wurde nicht gefunden.
    
- Die Konfigurationsdatei ist nicht lesbar.
    
- Die Konfigurationsdatei ist ungültig.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Clientanwendungen rufen die **IMAPIFormContainer::InstallForm-Methode** auf, um ein Formular in einem bestimmten Formularcontainer zu installieren. Der  _Parameter szCfgPathName_ muss den Pfad einer Formularkonfigurationsdatei enthalten (d. h. eine Datei mit der Erweiterung .cfg, die das Formular und dessen Implementierung beschreibt). Die Flags im  _ulFlags-Parameter_ geben Folgendes an: 
  
- Wenn das MAPI_DIALOG festgelegt ist, wird eine Benutzeroberfläche angezeigt, mit der der Benutzer, der das Formular installiert, Installationsdetails angeben kann.
    
- Wenn das MAPIFORM_INSTALL_OVERWRITEONCONFLICT festgelegt ist, wird jedes vorherige Formular für dieselbe Nachrichtenklasse durch das zu installierende Formular ersetzt. Andernfalls wird die Formularinstallation mit der aktuellen Formularbeschreibung zusammengeführt, sofern vorhanden.
    
- Wenn MAPI_DIALOG festgelegt ist, wird MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.
    
- Das Fehlen MAPIFORM_INSTALL_OVERWRITEONCONFLICT im Flagsatz bedeutet, dass eine Zusammenführung durchgeführt wird. Alle neuen Plattformen in der CFG-Datei, die derzeit nicht in der Formularbeschreibung vorhanden sind, werden installiert, und es werden keine weiteren Änderungen vorgenommen.
    
- Wenn das MAPI_UNICODE festgelegt ist, ist der Pfad der Formularkonfigurationsdatei eine Unicode-Zeichenfolge. 
    
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

