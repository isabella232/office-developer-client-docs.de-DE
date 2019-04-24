---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317409"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Konfiguriert einen Nachrichtendienst neu.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> in Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den zu konfigurierenden Nachrichtendienst enthält. 
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaften Blatts.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Anzeige des Eigenschaftenblatts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaften Blatt anzeigen, den Benutzer jedoch nicht ändern. Die meisten Nachrichtendienste ignorieren dieses Flag.
    
SERVICE_UI_ALLOWED 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaften Blatt nur anzeigen, wenn der Dienst nicht vollständig konfiguriert ist.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst muss immer sein Konfigurationseigenschaften Blatt anzeigen. Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Konfigurationseigenschaften Blatt weiterhin angezeigt werden, wenn SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen im Eigenschaftswert Array im _lpProps_ -Parameter nicht verfügbar sind. Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, damit ein Eigenschaftenblatt angezeigt wird. 
    
 _cValues_
  
> in Die Anzahl der Eigenschaftswerte in der [SPropValue](spropvalue.md) -Struktur, auf die durch _lpProps_verwiesen wird. 
    
 _lpProps_
  
> in Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die im Eigenschaftenfenster angezeigt werden sollen. Der _lpProps_ -Parameter sollte nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich konfiguriert.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein Fehler, der für einen Nachrichtendienst spezifisch ist. Zum Abrufen der [MAPIERROR](mapierror.md) -Struktur, die den Fehler beschreibt, sollte die Clientanwendung die [IMsgServiceAdmin:: getlasterroraufzurufen](imsgserviceadmin-getlasterror.md) -Methode aufrufen. 
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID** , auf die durch _lpUID_ verwiesen wird, stimmt nicht mit dem eines vorhandenen Nachrichtendiensts überein. 
    
MAPI_E_NOT_INITIALIZED 
  
> Der Nachrichtendienst verfügt nicht über eine Einstiegspunktfunktion.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenfenster. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMsgServiceAdmin:: ConfigureMsgService** -Methode kann ein Nachrichtendienst mit oder ohne Konfigurationseigenschaften Blatt konfiguriert werden. 
  
Um die Konfiguration ohne Eigenschaftenblatt Anzeige zuzulassen, bereiten Nachrichtendienste in der Regel eine Headerdatei vor, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die **MAPIUID** -Struktur für den Nachrichtendienst zum Konfigurieren abzurufen, rufen Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalte aus der Zeile des Nachrichtendiensts in der Nachrichtendienst Tabelle ab. Weitere Informationen finden Sie in der in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode beschriebenen Prozedur. 
  
Sie können einen Nachrichtendienst nur konfigurieren, ohne ein Eigenschaftenblatt für einen Benutzer anzuzeigen, wenn Sie über Vorabinformationen zu den festzulegenden Eigenschaftswerten verfügen. Wenn Sie einen Nachrichtendienst ohne Anzeige eines Eigenschaftenblatts konfigurieren, übergeben Sie gültige Eigenschaftswerte im _lpProps_ -Parameter, und legen Sie die Flags MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS nicht fest. 
  
Wenn Sie alle oder einen Teil der Konfigurationsinformationen des Benutzers über ein Eigenschaftenblatt erhalten, legen Sie SERVICE_UI_ALLOWED in _ulFlags_fest. Wenn Sie vorhandene Eigenschaftsinformationen nur zum Einrichten von Standardeinstellungen verwenden und der Benutzer in der Lage ist, die Einstellungen zu ändern, legen Sie SERVICE_UI_ALWAYS in _ulFlags_fest.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin:: ConfigureMsgService** -Methode, um einen Dienst zu konfigurieren, der einem Profil hinzugefügt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

