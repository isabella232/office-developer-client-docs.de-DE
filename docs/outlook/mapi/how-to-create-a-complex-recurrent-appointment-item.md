---
title: Erstellen eines komplexen Terminserienelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: da9626da-5ba5-4f18-954c-4e23971d23e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4087c02bcb827bf5e321706950af012386c9421f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610888"
---
# <a name="create-a-complex-recurrent-appointment-item"></a>Erstellen eines komplexen Terminserienelements
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann zum Erstellen von Terminserienelementen verwendet werden.
  
Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Installieren der in diesem Abschnitt verwendeten Beispiele.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-create-an-appointment-item"></a>So erstellen Sie ein Terminelement

1. Öffnen Sie einen Nachrichtenspeicher. Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen einer Nachricht Store](opening-a-message-store.md).
    
2. Öffnen Sie einen Kalenderordner im Nachrichtenspeicher. Siehe **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) im Kalenderordner auf, um das neue Terminelement zu erstellen. 
    
4. Legen Sie die **Eigenschaft dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) und andere Eigenschaften fest, die zum Erstellen eines Wiederkehrenden Termins erforderlich sind.
    
5. Speichern Sie das neue Terminelement.
    
Die  `AddAppointment` Funktion in der Quelldatei Appointments.cpp des Projekts CreateOutlookItemsAddin veranschaulicht diese Schritte. Die `AddAppointment` Funktion verwendet Parameter aus dem Dialogfeld **"Termin hinzufügen",** das angezeigt wird, wenn Sie im Menü **"Add-Ins"** in der MFCMAPI-Beispielanwendung auf **"Termin hinzufügen"** klicken. Die  `DisplayAddAppointmentDialog` Funktion in Appointments.cpp zeigt das Dialogfeld an und übergibt Werte aus dem Dialogfeld an die  `AddAppointment` Funktion. Die  `DisplayAddAppointmentDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Terminelements mithilfe der MAPI, daher wird sie hier nicht aufgeführt. 
  
> [!IMPORTANT]
> Der Code in der MFCMAPI-Anwendung stellt nicht sicher, dass der **Kalenderordner** ausgewählt wurde, wenn Sie im **Menü "Addins"** auf den Befehl **"Termin hinzufügen"** klicken. Das Erstellen eines Terminelements in einem anderen Ordner als dem **Kalenderordner** kann zu nicht definiertem Verhalten führen. Stellen Sie sicher, dass Sie den **Ordner "Kalender"** ausgewählt haben, bevor Sie den Befehl **"Termin hinzufügen"** in der MFCMAPI-Anwendung verwenden. 
  
Die  `AddAppointment` Methode ist unten aufgeführt. Beachten Sie, dass der an die Methode übergebene  _lpFolder-Parameter_  `AddAppointment` ein Zeiger auf eine [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) ist, die den Ordner darstellt, in dem der wiederkehrende Termin erstellt wird. Angesichts des  _lpFolder-Parameters,_ der eine **IMAPIFolder-Schnittstelle** darstellt, ruft der Code die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) auf. Die **CreateMessage-Methode** gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage-Schnittstelle** zurück. Der Großteil des `AddAppointment` Funktionscodes übernimmt die Arbeit beim Angeben von Eigenschaften in Vorbereitung auf den Aufruf der [IMAPIProp::SetProps-Methode.](imapiprop-setprops.md) Wenn der Aufruf der **SetProps-Methode** erfolgreich ist, wird die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen, um die Änderungen in den Speicher zu übernehmen und ein neues Kalenderelement zu erstellen. 
  
Die  `AddAppointment` Funktion legt eine Reihe benannter Eigenschaften fest. Informationen zu benannten Eigenschaften und deren Erstellung finden Sie unter [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx) Da die benannten Eigenschaften, die für Terminelemente verwendet werden, mehrere Eigenschaftensätze belegen, muss beim Erstellen von Parametern, die an die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) übergeben werden, mit Vorsicht vorgegangen werden. 
  
Die  `AddAppointment` Funktion verwendet mehrere Hilfsfunktionen, um eine Struktur für verschiedene terminbezogene Eigenschaften zu erstellen. Die  `BuildTimeZoneStruct` Funktionen und  `BuildTimeZoneDefinition` Hilfsfunktionen werden verwendet, um eine Struktur zu erstellen, die die zeitzonenbezogenen Eigenschaften angibt. Die zeitzonenbezogenen Eigenschaften sind **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)), and **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), and they are discussed in die entsprechenden Abschnitte von [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx). 

Die  `BuildGlobalObjectID` Funktion wird verwendet, um eine Struktur zu erstellen, die die **Eigenschaften LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) und **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) angibt, die in den entsprechenden Abschnitten von [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)erläutert werden. Die Struktur, die die **dispidApptRecur-Eigenschaft** angibt, wird mithilfe der  `BuildWeeklyAppointmentRecurrencePattern` Funktion erstellt. 

Informationen zu der von der Funktion erstellten Struktur `BuildWeeklyAppointmentRecurrencePattern` finden Sie unter [PidLidAppointmentRecur (kanonische Eigenschaft).](pidlidappointmentrecur-canonical-property.md) Beachten Sie, dass zwar eine vielzahl von Terminserienmustern möglich ist, die  `BuildWeeklyAppointmentRecurrencePattern` Funktion aber nur ein wöchentliches Terminserienmuster erstellt. Außerdem werden mehrere hartcodierte Werte verwendet, z. B. der Kalendertyp (Gregorianisch), der erste Wochentag (Sonntag) und die Anzahl der geänderten oder gelöschten Instanzen (keine). Eine allgemeinere Funktion zum Erstellen von Terminserienmustern müsste diese Variablen als Parameter akzeptieren. 
  
Es folgt die vollständige Auflistung der  `AddAppointment` Funktion. 
  
```cpp
HRESULT AddAppointment(LPMAPIFOLDER lpFolder,
               SYSTEMTIME* lpstStartDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstEndDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstStartFirstUST, // PidLidAppointmentStartWhole, PidLidCommonStart, PR_START_DATE
               SYSTEMTIME* lpstEndFirstUST, // PidLidAppointmentEndWhole, PidLidCommonEnd, PR_END_DATE
               SYSTEMTIME* lpszClipStartUST, // PidLidClipStart
               SYSTEMTIME* lpstClipEndUST, // PidLidClipEnd
               SYSTEMTIME* lpstFirstDOW, // PidLidAppointmentRecur
               DWORD dwStartOffsetLocal, // PidLidAppointmentRecur
               DWORD dwEndOffsetLocal, // PidLidAppointmentRecur
               DWORD dwPeriod, // PidLidAppointmentRecur
               DWORD dwOccurrenceCount, // PidLidAppointmentRecur
               DWORD dwPatternTypeSpecific, // PidLidAppointmentRecur
               ULONG ulDuration, // PidLidAppointmentDuration
               LPWSTR szSubject, // PR_SUBJECT_W
               LPWSTR szLocation, // PidLidLocation
               LPWSTR szPattern) // PidLidRecurrencePattern
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulAppointmentProps];
      LPMAPINAMEID rgpnmid[ulAppointmentProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulAppointmentProps ; i++)
      {
         if (i < ulFirstMeetingProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Appointment;
         else if (i < ulFirstCommonProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Meeting;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulAppointmentProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulAppointmentProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidAppointmentSequence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentSequence],PT_LONG);
         spvProps[p_PidLidBusyStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidBusyStatus],PT_LONG);
         spvProps[p_PidLidLocation].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidLocation],PT_UNICODE);
         spvProps[p_PidLidAppointmentStartWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentStartWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentEndWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentEndWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentDuration].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentDuration],PT_LONG);
         spvProps[p_PidLidAppointmentColor].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentColor],PT_LONG);
         spvProps[p_PidLidResponseStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidResponseStatus],PT_LONG);
         spvProps[p_PidLidRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurring],PT_BOOLEAN);
         spvProps[p_PidLidClipStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipStart],PT_SYSTIME);
         spvProps[p_PidLidClipEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipEnd],PT_SYSTIME);
         spvProps[p_PidLidTimeZoneStruct].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneStruct],PT_BINARY);
         spvProps[p_PidLidTimeZoneDescription].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneDescription],PT_UNICODE);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].ulPropTag
           = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionRecur],
           PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionStartDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionEndDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentRecur].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentRecur],PT_BINARY);
         spvProps[p_PidLidRecurrenceType].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrenceType],PT_LONG);
         spvProps[p_PidLidRecurrencePattern].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrencePattern],PT_UNICODE);
         spvProps[p_PidLidIsRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidIsRecurring],PT_BOOLEAN);
         spvProps[p_PidLidGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCleanGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCleanGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCommonStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonStart],PT_SYSTIME);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidSideEffects].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidSideEffects],PT_LONG);
         spvProps[p_PR_SUBJECT_W].ulPropTag          = PR_SUBJECT_W;
         spvProps[p_PR_START_DATE].ulPropTag         = PR_START_DATE;
         spvProps[p_PR_END_DATE].ulPropTag           = PR_END_DATE;
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag    = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag         = PR_ICON_INDEX;
         spvProps[p_PR_CONVERSATION_INDEX].ulPropTag   = PR_CONVERSATION_INDEX;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag      = PR_MESSAGE_FLAGS;
         spvProps[p_PidLidAppointmentSequence].Value.l = 0;
         spvProps[p_PidLidBusyStatus].Value.l = olBusy;
         spvProps[p_PidLidLocation].Value.lpszW = szLocation;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidAppointmentStartWhole].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidAppointmentEndWhole].Value.ft);
         spvProps[p_PidLidAppointmentDuration].Value.l = ulDuration;
         spvProps[p_PidLidAppointmentColor].Value.l = 0; // No color
         spvProps[p_PidLidResponseStatus].Value.l = respNone;
         spvProps[p_PidLidRecurring].Value.b = true;
         SystemTimeToFileTime(lpszClipStartUST,&spvProps[p_PidLidClipStart].Value.ft);
         SystemTimeToFileTime(lpstClipEndUST,&spvProps[p_PidLidClipEnd].Value.ft);
         SYSTEMTIME stStandard = {0};
         stStandard.wMonth = 0xB;
         stStandard.wDay = 0x1;
         stStandard.wHour = 0x2;
         SYSTEMTIME stDaylight = {0};
         stDaylight.wMonth = 0x3;
         stDaylight.wDay = 0x2;
         stDaylight.wHour = 0x2;
         hRes = BuildTimeZoneStruct(
            300,
            0,
            (DWORD)-60,
            &stStandard,
            &stDaylight,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.cb,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb);
         spvProps[p_PidLidTimeZoneDescription].Value.lpszW = L"(GMT-05:00) Eastern Time (US & Canada)";
         SYSTEMTIME stRule1Standard = {0};
         stRule1Standard.wMonth = 0xA;
         stRule1Standard.wDay = 0x5;
         stRule1Standard.wHour = 0x2;
         SYSTEMTIME stRule1Daylight = {0};
         stRule1Daylight.wMonth = 0x4;
         stRule1Daylight.wDay = 0x1;
         stRule1Daylight.wHour = 0x2;
         if (SUCCEEDED(hRes)) hRes = BuildTimeZoneDefinition(
            L"Eastern Standard Time",
            0, // TZRule Flags
            2006, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stRule1Standard, // stStandardDate
            &stRule1Daylight, // stDaylightDate
            TZRULE_FLAG_EFFECTIVE_TZREG, // TZRule Flags
            2007, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stStandard, // stStandardDate
            &stDaylight, // stDaylightDate
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         if (SUCCEEDED(hRes)) hRes = BuildWeeklyAppointmentRecurrencePattern(
            lpstStartDateLocal,
            lpstEndDateLocal,
            lpstFirstDOW,
            dwStartOffsetLocal,
            dwEndOffsetLocal,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.lpb);
         spvProps[p_PidLidRecurrenceType].Value.l = rectypeWeekly;
         spvProps[p_PidLidRecurrencePattern].Value.lpszW = szPattern;
         spvProps[p_PidLidIsRecurring].Value.b = true;
         if (SUCCEEDED(hRes)) hRes = BuildGlobalObjectId(
            &spvProps[p_PidLidGlobalObjectId].Value.bin.cb,
            &spvProps[p_PidLidGlobalObjectId].Value.bin.lpb);
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.cb  = spvProps[p_PidLidGlobalObjectId].Value.bin.cb;
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.lpb = spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidCommonStart].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidSideEffects].Value.l
            = seOpenToDelete | seOpenToCopy | seOpenToMove | seCoerceToInbox | seOpenForCtxMenu;
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PR_START_DATE].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PR_END_DATE].Value.ft);
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Appointment";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x00000401; // Recurring Appointment
         if (SUCCEEDED(hRes)) hRes = BuildConversationIndex(
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         if (SUCCEEDED(hRes)) hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SaveChanges(FORCE_SAVE);
         }
         if (spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb)
            delete[] spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb;
         if (spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionStartDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionEndDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         if (spvProps[p_PidLidAppointmentRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentRecur].Value.bin.lpb;
         if (spvProps[p_PidLidGlobalObjectId].Value.bin.lpb)
            delete[] spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         // Do not delete p_PidLidCleanGlobalObjectId, it was borrowed from p_PidLidGlobalObjectId
         if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
            delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>Siehe auch

- [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

