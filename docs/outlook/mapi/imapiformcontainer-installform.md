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
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, die Clientanwendung legt das MAPI_DIALOG-Flag im _ulFlags_ -Parameter fest. Der _ulUIParam_ -Parameter kann NULL sein, wenn MAPI_DIALOG nicht ebenfalls übergeben wird. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Installation des Formulars steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, um Statusinformationen bereitzustellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt.
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Wenn bereits ein anderes Formular vorhanden ist, das die von diesem Formular behandelte Nachrichtenklasse behandelt, ersetzen Sie das vorhandene Formular durch dieses. Dieses Flag wird ignoriert, wenn auch das MAPI_DIALOG-Flag vorhanden ist. 
    
 _szCfgPathName_
  
> in Der Pfad zur Konfigurationsdatei des Formulars.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein Implementierungsfehler ist aufgetreten. Rufen Sie die [IMAPIFormContainer:: getlasterroraufzurufen](imapiformcontainer-getlasterror.md) -Methode auf, um die [MAPIERROR](mapierror.md) -Struktur abzurufen, die dem Fehler zugeordnet ist. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat die Installation des Formulars abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Anbieter von Formularbibliotheken sollten eine **MAPIERROR** -Struktur ausfüllen und MAPI_E_EXTENDED_ERROR zurückgeben, wenn eine der folgenden Bedingungen eintritt: 
  
- Die Konfigurationsdatei wurde nicht gefunden.
    
- Die Konfigurationsdatei ist nicht lesbar.
    
- Die Konfigurationsdatei ist ungültig.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Client Anwendungen rufen die **IMAPIFormContainer:: InstallForm** -Methode auf, um ein Formular in einem bestimmten Formular Container zu installieren. Der Parameter _szCfgPathName_ muss den Pfad einer Formular Konfigurationsdatei enthalten (also eine Datei mit der Erweiterung. cfg, die das Formular und die Implementierung beschreibt). Die Flags im Parameter _ulFlags_ geben Folgendes an: 
  
- Wenn das MAPI_DIALOG-Flag festgelegt ist, wird eine Benutzeroberfläche angezeigt, die es dem Benutzer, der das Formular installiert, ermöglicht, Installationsdetails anzugeben.
    
- Wenn das MAPIFORM_INSTALL_OVERWRITEONCONFLICT-Flag festgelegt ist, wird jedes vorherige Formular für dieselbe Nachrichtenklasse durch das installierte Formular ersetzt. Andernfalls wird die Formular Installation mit der aktuellen Formularbeschreibung zusammengeführt, sofern vorhanden.
    
- Wenn MAPI_DIALOG festgelegt ist, wird MAPIFORM_INSTALL_OVERWRITEONCONFLICT ignoriert.
    
- Das Fehlen von MAPIFORM_INSTALL_OVERWRITEONCONFLICT im Flagsatz bewirkt, dass ein Mergevorgang durchgeführt wird. Alle neuen Plattformen in der CFG-Datei, die derzeit nicht in der Formularbeschreibung enthalten sind, werden installiert, und es werden keine weiteren Änderungen vorgenommen.
    
- Wenn das MAPI_UNICODE-Flag festgelegt ist, ist der Pfad der Formular Konfigurationsdatei eine Unicode-Zeichenfolge. 
    
Clients sollten [IMAPIFormContainer:: getlasterroraufzurufen](imapiformcontainer-getlasterror.md) aufrufen, wenn **InstallForm** MAPI_E_EXTENDED_ERROR zurückgibt, und Sie sollten die zurückgegebene [MAPIERROR](mapierror.md) -Struktur überprüfen, um die Bedingung zu ermitteln, die den Fehler ausgelöst hat. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnInstallForm  <br/> |MFCMAPI verwendet die **IMAPIFormContainer:: InstallForm** -Methode, um ein Formular in einem Formular Container zu installieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

