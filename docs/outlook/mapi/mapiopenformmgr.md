---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270098"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle für ein Formularbibliothek-Anbieterobjekt im Kontext einer vorhandenen Sitzung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Parameter

 _pSession_
  
> in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird.
    
 _ppmgr_
  
> Out Zeiger auf die zurückgegebene **IMAPIFormMgr** -Schnittstelle. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Nachdem eine Clientanwendung die **MAPIOpenFormMgr** -Funktion aufgerufen hat, erfolgen die meisten nachfolgenden formularbezogenen Interaktionen über den Formularbibliothek Anbieter oder eine vom Formular Bibliotheks Anbieter zurückgegebene Schnittstelle. Die **IMAPIFormMgr** -Schnittstelle ermöglicht es dem Client, mit Nachrichten Handlern zu arbeiten und Lösungen zwischen Nachrichtenklassen und Formularbibliotheken auszuführen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg. cpp öffnet den Formular-Manager, damit ein Formular ausgewählt werden kann.  <br/> |CMainDlg:: OnSelectForm  <br/> |MFCMAPI verwendet die **MAPIOpenFormMgr** -Methode, um den Formular-Manager zu öffnen, damit ein Formular ausgewählt werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

