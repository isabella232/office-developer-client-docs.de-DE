---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 891b2f91042ba920f309ec3f9ae10077149151f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600820"
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
  
> [in] Ein Zeiger auf die [MAPIUID-Struktur,](mapiuid.md) die den eindeutigen Bezeichner für den zu konfigurierenden Nachrichtendienst enthält. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaftenfensters.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Anzeige des Eigenschaftenblatts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaftenblatt anzeigen, den Benutzer jedoch nicht in der Lage machen, ihn zu ändern. Die meisten Nachrichtendienste ignorieren dieses Kennzeichen.
    
SERVICE_UI_ALLOWED 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaftenblatt nur anzeigen, wenn der Dienst nicht vollständig konfiguriert ist.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst muss immer sein Konfigurationseigenschaftenblatt anzeigen. Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Konfigurationseigenschaftsblatt weiterhin angezeigt werden, wenn SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen im Eigenschaftswertarray im  _lpProps-Parameter_ nicht verfügbar sind. Es muss entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS festgelegt werden, damit ein Eigenschaftenblatt angezeigt wird. 
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die von  _lpProps_ verwiesen wird. 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftswerten, die die im Eigenschaftenblatt anzuzeigenden Eigenschaften beschreiben. Der  _parameter lpProps_ sollte nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich konfiguriert.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein für einen Nachrichtendienst spezifischer Fehler. Um die [MAPIERROR-Struktur](mapierror.md) abzurufen, die den Fehler beschreibt, sollte die Clientanwendung die [IMsgServiceAdmin::GetLastError-Methode](imsgserviceadmin-getlasterror.md) aufrufen. 
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die von  _lpUID_ verwiesen wird, stimmt nicht mit der eines vorhandenen Nachrichtendiensts überein. 
    
MAPI_E_NOT_INITIALIZED 
  
> Der Nachrichtendienst verfügt nicht über eine Einstiegspunktfunktion.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenblatt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::ConfigureMsgService-Methode** ermöglicht die Konfiguration eines Nachrichtendiensts mit oder ohne Konfigurationseigenschaftenblatt. 
  
Um die Konfiguration ohne Anzeige eines Eigenschaftenblatts zuzulassen, bereiten Nachrichtendienste in der Regel eine Headerdatei vor, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die **MAPIUID-Struktur** für den zu konfigurierenden Nachrichtendienst abzurufen, rufen Sie die **Spalte PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab. Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode](imsgserviceadmin-createmsgservice.md) beschriebenen Prozedur. 
  
Sie können einen Nachrichtendienst nur dann konfigurieren, wenn einem Benutzer ein Eigenschaftenblatt angezeigt wird, wenn Sie vorab Informationen zu den festzulegenden Eigenschaftswerten haben. Wenn Sie einen Nachrichtendienst konfigurieren, ohne ein Eigenschaftenblatt anzuzeigen, übergeben Sie gültige Eigenschaftswerte im  _lpProps-Parameter,_ und legen Sie die Flags MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS nicht fest. 
  
Wenn Sie alle oder einige der Konfigurationsinformationen vom Benutzer über ein Eigenschaftenblatt erhalten, legen Sie SERVICE_UI_ALLOWED in  _ulFlags_ fest. Wenn Sie vorhandene Eigenschafteninformationen nur zum Einrichten von Standardeinstellungen verwenden und der Benutzer die Einstellungen ändern kann, legen Sie SERVICE_UI_ALWAYS in  _ulFlags_ fest.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::ConfigureMsgService-Methode,** um einen Dienst zu konfigurieren, der einem Profil hinzugefügt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

