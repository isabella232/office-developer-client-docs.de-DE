---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430679"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Einstiegspunktfunktion des Dienstanbieters, die vom Profil-Assistenten aufgerufen wird, um genügend Informationen zum Anzeigen der Konfigurationseigenschaftsblätter des Anbieters abzurufen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parameter

 _hProviderDLLInstance_
  
> [in] Instanzhandle der DLL des Dienstanbieters. 
    
 _lpcsResourceName_
  
> [out] Zeiger auf eine Zeichenfolge, die den vollständigen Namen der Dialogressource enthält, die während der Konfiguration vom Profil-Assistenten angezeigt werden soll. Die maximale Größe der Zeichenfolge, einschließlich des NULL-Abschlusszeichens, beträgt 32 Zeichen. 
    
 _lppDlgProc_
  
> [out] Zeiger auf eine standardmäßige Windows, die vom Profil-Assistenten aufgerufen wird, um den Anbieter über verschiedene Ereignisse zu benachrichtigen. 
    
 _lpMAPIProp_
  
> [in] Zeiger auf eine Eigenschaftsschnittstellenimplementierung, die Zugriff auf die Konfigurationseigenschaften bietet. 
    
 _lpMapiSupportObject_
  
> [in] Zeiger auf das MAPI-Unterstützungsobjekt, das für diese Sitzung gilt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **WIZARDENTRY-Funktion** des Dienstanbieters wurde erfolgreich aufgerufen. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs.
    
## <a name="remarks"></a>Hinweise

Der Profil-Assistent ruft die **WIZARDENTRY-basierte** Funktion auf, wenn die Konfigurationsbenutzerschnittstelle des Dienstanbieters angezeigt werden kann. Wenn der Profil-Assistent alle Anbieter konfiguriert hat, schreibt er die Konfigurationseigenschaften in das Profil, indem er [IMsgServiceAdmin::ConfigureMsgService aufruft.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Name der **WIZARDENTRY-basierten** Funktion muss im WIZARD_ENTRY_NAME MAPISVC.INF platziert werden. 
  
Der Ressourcenname ist der der Dialogfeldressource, die im Bereich des Profil-Assistenten gerendert wird. Die übergebene Ressource muss alle Seiten in einer einzelnen Dialogressource enthalten. Wenn der Profil-Assistent diese Ressource empfängt, ignoriert er die Dialogformatvorlage, aber nicht die Steuerelementformatvorlagen und erstellt alle Steuerelemente als untere Steuerelemente der Seite Profil-Assistent. Alle Steuerelemente werden zunächst ausgeblendet. Anbieter sollten sicherstellen, dass die Koordinaten für ihre Steuerelemente null- oder nullbasierte Sind und eine maximale Breite von 200 Dialogeinheiten und eine maximale Höhe von 150 Dialogeinheiten nicht überschreiten. Steuerelementbezeichner unter 400 sind für den Profil-Assistenten reserviert. Der Profil-Assistent zeigt den Titel des Anbieters in fett formatierten Text über der Benutzeroberfläche des Anbieters an. 
  
Der im  _lpMAPIProp-Parameter_ bereitgestellte Eigenschaftsschnittstellenzeiger sollte vom Anbieter für zukünftige Verweise beibehalten werden. Der Profil-Assistent behandelt nur die grundlegendsten Eigenschaften, und der Anbieter kann die Implementierung der Eigenschaftenschnittstelle verwenden, um zusätzliche Eigenschaften zu enthalten. Während der Konfiguration sollten Anbieter dem Objekt, das die Eigenschaftsschnittstelle implementiert, ihre Konfigurationseigenschaften hinzufügen. Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften dem Profil hinzu. 
  
Weitere Informationen zur Verwendung dieser Funktion finden Sie unter [Supporting Message Service Configuration](supporting-message-service-configuration.md). 
  

