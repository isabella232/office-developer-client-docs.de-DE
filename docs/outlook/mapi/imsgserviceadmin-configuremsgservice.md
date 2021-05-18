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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422187"
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
  
> [in] Ein Handle zum übergeordneten Fenster des Konfigurationseigenschaftsblatts.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Anzeige des Eigenschaftenblatts steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaftsblatt anzeigen, aber dem Benutzer nicht ermöglichen, es zu ändern. Die meisten Nachrichtendienste ignorieren dieses Kennzeichen.
    
SERVICE_UI_ALLOWED 
  
> Der Nachrichtendienst sollte sein Konfigurationseigenschaftsblatt nur dann anzeigen, wenn der Dienst nicht vollständig konfiguriert ist.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst muss immer sein Konfigurationseigenschaftsblatt anzeigen. Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann weiterhin ein Konfigurationseigenschaftenblatt angezeigt werden, wenn SERVICE_UI_ALLOWED festgelegt ist und keine gültigen Konfigurationsinformationen im Eigenschaftswertarray im  _lpProps-Parameter verfügbar_ sind. Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, damit ein Eigenschaftenblatt angezeigt wird. 
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der [SPropValue-Struktur,](spropvalue.md) auf die von _lpProps verwiesen wird._ 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftswerten, die die eigenschaften beschreiben, die im Eigenschaftenblatt angezeigt werden. Der  _lpProps-Parameter_ sollte nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich konfiguriert.
    
MAPI_E_EXTENDED_ERROR 
  
> Ein für einen Nachrichtendienst spezifischer Fehler. Um die [MAPIERROR-Struktur](mapierror.md) zu erhalten, die den Fehler beschreibt, sollte die Clientanwendung die [IMsgServiceAdmin::GetLastError-Methode](imsgserviceadmin-getlasterror.md) aufrufen. 
    
MAPI_E_NOT_FOUND 
  
> Die **MAPIUID,** auf die  _von lpUID_ verwiesen wird, ist nicht mit der eines vorhandenen Nachrichtendiensts übereinstimmend. 
    
MAPI_E_NOT_INITIALIZED 
  
> Der Nachrichtendienst verfügt nicht über eine Einstiegspunktfunktion.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenblatt. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::ConfigureMsgService-Methode** ermöglicht die Konfiguration eines Nachrichtendiensts mit oder ohne Konfigurationseigenschaftsblatt. 
  
Um die Konfiguration ohne Anzeige eines Eigenschaftenblatts zu ermöglichen, bereiten Nachrichtendienste in der Regel eine Headerdatei vor, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die **MAPIUID-Struktur** für den zu konfigurierenden Nachrichtendienst abzurufen, rufen Sie die **Spalte PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) aus der Zeile des Nachrichtendiensts in der Nachrichtendiensttabelle ab. Weitere Informationen finden Sie in der in der [IMsgServiceAdmin::CreateMsgService-Methode beschriebenen](imsgserviceadmin-createmsgservice.md) Prozedur. 
  
Sie können einen Nachrichtendienst konfigurieren, ohne einem Benutzer nur dann ein Eigenschaftenblatt anzeigen zu müssen, wenn Sie vorab Informationen zu den zu setzenden Eigenschaftswerten haben. Wenn Sie einen Nachrichtendienst konfigurieren, ohne ein Eigenschaftenblatt anzeigen zu müssen, übergeben Sie gültige Eigenschaftswerte im  _lpProps-Parameter,_ und legen Sie keine MSG_SERVICE_UI_READ_ONLY-, SERVICE_UI_ALLOWED- oder SERVICE_UI_ALWAYS-Flags. 
  
Wenn Sie alle oder einige Konfigurationsinformationen über ein Eigenschaftenblatt vom Benutzer erhalten, legen Sie SERVICE_UI_ALLOWED _ulFlags ._ Wenn Sie vorhandene Eigenschaftsinformationen nur zum Einrichten von Standardeinstellungen verwenden und der Benutzer die Einstellungen ändern kann, legen Sie SERVICE_UI_ALWAYS _ulFlags fest._
  
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

