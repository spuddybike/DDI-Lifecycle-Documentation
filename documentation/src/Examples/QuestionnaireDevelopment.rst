Questionnaire Development
==========================
    
.. code-block:: XML
    
  <?xml version="1.0" encoding="UTF-8"?>
  <!--
    
  Example - Questionnaire Development
    
  -->
    
    <g:ResourcePackage xmlns:ddi="ddi:instance:3_3" xmlns:a="ddi:archive:3_3" xmlns:c="ddi:conceptualcomponent:3_3" xmlns:cm="ddi:comparative:3_3" xmlns:d="ddi:datacollection:3_3" xmlns:g="ddi:group:3_3" xmlns:l="ddi:logicalproduct:3_3" xmlns:p="ddi:physicaldataproduct:3_3" xmlns:pi="ddi:physicalinstance:3_3" xmlns:pr="ddi:ddiprofile:3_3" xmlns:r="ddi:reusable:3_3" xmlns:s="ddi:studyunit:3_3" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="ddi:instance:3_3 ../../XMLSchema/instance.xsd">
      <r:URN>urn:ddi:us.mpc:RP:1</r:URN>
      <d:DataCollection isMaintainable="true" scopeOfUniqueness="Agency">
        <r:URN>urn:ddi:us.mpc:DColl:1</r:URN>
        <d:QuestionnaireDevelopment isVersionable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:QDev:1</r:URN>
          <d:DevelopmentPlan isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:DevPlan_1:1</r:URN>
            <d:DevelopmentObjective><r:Content>Validate the consistency of the response to this question across translations.   
            </r:Content></d:DevelopmentObjective>
            <d:DevelopmentObjectReference>
              <r:URN>urn:ddi:us.mpc:Q_1e:1</r:URN>
              <r:TypeOfObject>QuestionItem</r:TypeOfObject>
            </d:DevelopmentObjectReference>
            <d:DevelopmentActivityReference>
              <r:URN>urn:ddi:us.mpc:TransAct_1:1</r:URN>
              <r:TypeOfObject>TranslationActivity</r:TypeOfObject>
            </d:DevelopmentActivityReference>
            <d:DevelopmentActivityReference>
              <r:URN>urn:ddi:us.mpc:ContRev_1:1</r:URN>
              <r:TypeOfObject>ContentReviewActivity</r:TypeOfObject>
            </d:DevelopmentActivityReference>
            <d:DevelopmentActivityReference>
              <r:URN>urn:ddi:us.mpc:CogExp_1:1</r:URN>
              <r:TypeOfObject>CognitiveExpertReviewActivity</r:TypeOfObject>
            </d:DevelopmentActivityReference>
          </d:DevelopmentPlan>
          <d:DevelopmentProcess isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:DevProcess_1:1</r:URN>
            <d:DevelopmentPlanReference>
              <r:URN>urn:ddi:us.mpc:DevPlan_1:1</r:URN>
              <r:TypeOfObject>DevelopmentPlan</r:TypeOfObject>
            </d:DevelopmentPlanReference>
            <d:DevelopmentProcessStep isIdentifiable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:DPStep_1:1</r:URN>
              <d:SuccessorStepReference>
                <r:URN>urn:ddi:us.mpc:DPStep_2:1</r:URN>
                <r:TypeOfObject>DevelopmentProcessStep</r:TypeOfObject>
              </d:SuccessorStepReference>
              <d:DevelopmentObjectReference>
                <r:URN>urn:ddi:us.mpc:Q_1e:1</r:URN>
                <r:TypeOfObject>QuestionItem</r:TypeOfObject>
              </d:DevelopmentObjectReference>
              <d:DevelopmentActivityReference>
                <r:URN>urn:ddi:us.mpc:ContRev_1:1</r:URN>
                <r:TypeOfObject>ContentReviewActivity</r:TypeOfObject>
              </d:DevelopmentActivityReference>
              <d:ConditionForAcceptance><r:Content>Concensus of evaluators that a consistent response is obtained from the question.</r:Content></d:ConditionForAcceptance>
              <d:ActivityDate>
                <r:StartDate>2013-03-01</r:StartDate>
                <r:EndDate>2013-04-01</r:EndDate>
              </d:ActivityDate>
            </d:DevelopmentProcessStep>
            <d:DevelopmentProcessStep isIdentifiable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:DPStep_2:1</r:URN>
              <d:PredecessorStepReference>
                <r:URN>urn:ddi:us.mpc:DPStep_1:1</r:URN>
                <r:TypeOfObject>DevelopmentProcessStep</r:TypeOfObject>
              </d:PredecessorStepReference>
              <d:SuccessorStepReference>
                <r:URN>urn:ddi:us.mpc:DPStep_3:1</r:URN>
                <r:TypeOfObject>DevelopmentProcessStep</r:TypeOfObject>
              </d:SuccessorStepReference>
              <d:DevelopmentObjectReference>
                <r:URN>urn:ddi:us.mpc:Q_1e:1</r:URN>
                <r:TypeOfObject>QuestionItem</r:TypeOfObject>
              </d:DevelopmentObjectReference>
              <d:DevelopmentActivityReference>
                <r:URN>urn:ddi:us.mpc:TransAct_1:1</r:URN>
                <r:TypeOfObject>TranslationActivity</r:TypeOfObject>
              </d:DevelopmentActivityReference>
              <d:ConditionForAcceptance><r:Content>Experts statement of completion.</r:Content></d:ConditionForAcceptance>
              <d:ActivityDate>
                <r:StartDate>2013-04-02</r:StartDate>
                <r:EndDate>2013-04-10</r:EndDate>
              </d:ActivityDate>
            </d:DevelopmentProcessStep>
            <d:DevelopmentProcessStep isIdentifiable="true" scopeOfUniqueness="Agency">
              <r:URN>urn:ddi:us.mpc:DPStep_3:1</r:URN>
              <d:PredecessorStepReference>
                <r:URN>urn:ddi:us.mpc:DPStep_2:1</r:URN>
                <r:TypeOfObject>DevelopmentProcessStep</r:TypeOfObject>
              </d:PredecessorStepReference>
              <d:DevelopmentObjectReference>
                <r:URN>urn:ddi:us.mpc:Q_1e:1</r:URN>
                <r:TypeOfObject>QuestionItem</r:TypeOfObject>
              </d:DevelopmentObjectReference>
              <d:DevelopmentActivityReference>
                <r:URN>urn:ddi:us.mpc:CogExp_1:1</r:URN>
                <r:TypeOfObject>CognitiveExpertReviewActivity</r:TypeOfObject>
              </d:DevelopmentActivityReference>
              <d:ConditionForAcceptance><r:Content>Concensus of evaluators that a consistent response is obtained from the question for each language.</r:Content></d:ConditionForAcceptance>
              <d:ActivityDate>
                <r:StartDate>2013-04-11</r:StartDate>
                <r:EndDate>2013-04-30</r:EndDate>
              </d:ActivityDate>
            </d:DevelopmentProcessStep>
          </d:DevelopmentProcess>
          <d:DevelopmentResults isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:DResults_1:1</r:URN>
            <r:Description><r:Content></r:Content></r:Description>
          </d:DevelopmentResults>
        </d:QuestionnaireDevelopment>
        <d:QuestionScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:QScheme:1</r:URN>
          <d:QuestionItem isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:Q_1e:1</r:URN>
            <d:QuestionText audienceLanguage="en" isStructureRequired="false">
              <d:LiteralText><d:Text xml:lang="en">What is your name?</d:Text></d:LiteralText>
            </d:QuestionText>
            <d:TextDomain blankIsMissingValue="true" minLength="0" maxLength="50"/>
          </d:QuestionItem>
        </d:QuestionScheme>
        <d:DevelopmentActivityScheme isMaintainable="true" scopeOfUniqueness="Agency">
          <r:URN>urn:ddi:us.mpc:DevActScheme:1</r:URN>
          <d:ContentReviewActivity isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:ContRev_1:1</r:URN>
            <r:Description><r:Content>Evaluation of specific question language and comparability of responses across major cultural groups.</r:Content></r:Description>
            <d:DesiredOutcome><r:Content>Verification that the the content of a question elicits consistent comparable responses.</r:Content></d:DesiredOutcome>
            <d:RecommendedStaffRequirements>
              <d:StaffClass>DevelopmentTeam</d:StaffClass>
              <d:ParticipantRequirements><r:Content>Knowledge of question intent. Knowledge of question testing of various types within major cultural groups.</r:Content></d:ParticipantRequirements>
            </d:RecommendedStaffRequirements>
            <d:TypeOfContentReview>TeamReview</d:TypeOfContentReview>
          </d:ContentReviewActivity>
          <d:CognitiveExpertReviewActivity isVersionable="true" scopeOfUniqueness="Agency">
            <r:URN>urn:ddi:us.mpc:CogExp_1:1</r:URN>
            <r:Description><r:Content>Evaluation of all question languages and comparability of responses across major cultural groups.</r:Content></r:Description>
            <d:DesiredOutcome><r:Content>Verification that the the content of a question elicits consistent comparable responses.</r:Content></d:DesiredOutcome>
            <d:RecommendedStaffRequirements>
              <d:StaffClass>QualityEvaluator</d:StaffClass>
              <d:ParticipantRequirements><r:Content>Experience with the effect of question wording on response for open ended question types. Knowledge of question testing of various types within major cultural groups.</r:Content>
              </d:ParticipantRequirements>
            </d:RecommendedStaffRequirements>
            <d:TypeOfCognitiveExpertReview>CrossLanguageConsistency</d:TypeOfCognitiveExpertReview>
          </d:CognitiveExpertReviewActivity>
          <d:TranslationActivity isVersionable="true" scopeOfUniqueness="Agency" translationSourceLanguage="en" translationTargetLanguage="de">
            <r:URN>urn:ddi:us.mpc:TransAct_1:1</r:URN>
            <d:TranslationMethod>
              <d:TypeOfTranslationMethod>LiteralTranslation</d:TypeOfTranslationMethod>
            </d:TranslationMethod>
            <d:TranslationRequirements isOral="false" isWritten="true"><r:Content>Accurate translation from source to target language validated by content review.</r:Content></d:TranslationRequirements>
            <d:TranslatorRequirements>
              <d:TranslationSourceLanguageAbility>
                <d:MinimumLanguageAbility>
                  <r:Language>English</r:Language>
                  <a:Read controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Full Professonal Proficiency</a:Read>
                  <a:Write controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Full Professonal Proficiency</a:Write>
                </d:MinimumLanguageAbility>
                <d:PreferredLanguageAbility>
                  <r:Language>English</r:Language>
                  <a:Read controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Native or Bilingual Proficiency</a:Read>
                  <a:Write controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Native or Bilingual Proficiency</a:Write>
                </d:PreferredLanguageAbility>
              </d:TranslationSourceLanguageAbility>
              <d:TranslationTargetLanguageAbility>
                <d:MinimumLanguageAbility>
                  <r:Language>German</r:Language>
                  <a:Read controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Full Professonal Proficiency</a:Read>
                  <a:Write controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Full Professonal Proficiency</a:Write>
                </d:MinimumLanguageAbility>
                <d:PreferredLanguageAbility>
                  <r:Language>German</r:Language>
                  <a:Read controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Native or Bilingual Proficiency</a:Read>
                  <a:Write controlledVocabularyURN="http://careers.state.gov/gateway/lang_prof_def.html">Native or Bilingual Proficiency</a:Write>
                </d:PreferredLanguageAbility>
              </d:TranslationTargetLanguageAbility>
            </d:TranslatorRequirements>
          </d:TranslationActivity>
        </d:DevelopmentActivityScheme>
      </d:DataCollection>
    </g:ResourcePackage>
