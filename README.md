1. Запуск Rasa в режиме debug для сбора логов: `rasa run --enable-api --debug --cors "*"`
2. [Скриншот диалога](./screenshot.png)
3. [Файл с debug логами Rasa](./rasa.log)



<details>

<summary>Показать лог</summary>

```bush
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/rasa/shared/utils/validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/pkg_resources/__init__.py:3154: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('mpl_toolkits')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/pkg_resources/__init__.py:3154: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('ruamel')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
<frozen importlib._bootstrap>:283: DeprecationWarning: the load_module() method is deprecated and slated for removal in Python 3.12; use exec_module() instead
2024-10-26 20:48:22 DEBUG    rasa.cli.utils  - Parameter 'credentials' not set. Using default location 'credentials.yml' instead.
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/sanic_cors/extension.py:39: DeprecationWarning: distutils Version classes are deprecated. Use packaging.version instead.
  SANIC_VERSION = LooseVersion(sanic_version)
2024-10-26 20:48:23 DEBUG    h5py._conv  - Creating converter from 7 to 5
2024-10-26 20:48:23 DEBUG    h5py._conv  - Creating converter from 5 to 7
2024-10-26 20:48:23 DEBUG    h5py._conv  - Creating converter from 7 to 5
2024-10-26 20:48:23 DEBUG    h5py._conv  - Creating converter from 5 to 7
2024-10-26 20:48:24 DEBUG    jax._src.path  - etils.epath was not found. Using pathlib for file I/O.
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/tensorflow/lite/python/util.py:52: DeprecationWarning: jax.xla_computation is deprecated. Please use the AOT APIs.
  from jax import xla_computation as _xla_computation
<frozen importlib._bootstrap>:283: DeprecationWarning: the load_module() method is deprecated and slated for removal in Python 3.12; use exec_module() instead
2024-10-26 20:48:25 DEBUG    rasa.core.utils  - Available web server routes:
/conversations/<conversation_id:path>/messages     POST                           add_message
/conversations/<conversation_id:path>/tracker/events POST                           append_events
/webhooks/rasa                                     GET                            custom_webhook_RasaChatInput.health
/webhooks/rasa/webhook                             POST                           custom_webhook_RasaChatInput.receive
/webhooks/rest                                     GET                            custom_webhook_RestInput.health
/webhooks/rest/webhook                             POST                           custom_webhook_RestInput.receive
/model/test/intents                                POST                           evaluate_intents
/model/test/stories                                POST                           evaluate_stories
/conversations/<conversation_id:path>/execute      POST                           execute_action
/domain                                            GET                            get_domain
/                                                  GET                            hello
/model                                             PUT                            load_model
/model/parse                                       POST                           parse
/conversations/<conversation_id:path>/predict      POST                           predict
/conversations/<conversation_id:path>/tracker/events PUT                            replace_events
/conversations/<conversation_id:path>/story        GET                            retrieve_story
/conversations/<conversation_id:path>/tracker      GET                            retrieve_tracker
/status                                            GET                            status
/model/predict                                     POST                           tracker_predict
/model/train                                       POST                           train
/conversations/<conversation_id:path>/trigger_intent POST                           trigger_intent
/model                                             DELETE                         unload_model
/version                                           GET                            version
2024-10-26 20:48:25 INFO     root  - Starting Rasa server on http://0.0.0.0:5005
2024-10-26 20:48:25 DEBUG    rasa.core.utils  - Using the default number of Sanic workers (1).
2024-10-26 20:48:26 DEBUG    rasa.telemetry  - Skipping telemetry reporting: no license hash found.
2024-10-26 20:48:26 DEBUG    rasa.core.tracker_store  - Connected to InMemoryTrackerStore.
2024-10-26 20:48:26 DEBUG    rasa.core.lock_store  - Connected to lock store 'InMemoryLockStore'.
2024-10-26 20:48:26 DEBUG    rasa.core.nlg.generator  - Instantiated NLG to 'TemplatedNaturalLanguageGenerator'.
2024-10-26 20:48:26 INFO     rasa.core.processor  - Loading model models/20241026-202103-tranquil-raster.tar.gz...
2024-10-26 20:48:26 DEBUG    rasa.engine.storage.local_model_storage  - Extracted model to '/tmp/tmpcpkrrnzs'.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' loading 'NLUMessageConverter.load' and kwargs: '{}'.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' loading 'WhitespaceTokenizer.load' and kwargs: '{}'.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' loading 'RegexFeaturizer.load' and kwargs: '{}'.
2024-10-26 20:48:26 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RegexFeaturizer1' was requested for reading.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' loading 'LexicalSyntacticFeaturizer.load' and kwargs: '{}'.
2024-10-26 20:48:26 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_LexicalSyntacticFeaturizer2' was requested for reading.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' loading 'CountVectorsFeaturizer.load' and kwargs: '{}'.
2024-10-26 20:48:26 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_CountVectorsFeaturizer3' was requested for reading.
2024-10-26 20:48:26 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' loading 'LanguageModelFeaturizer.load' and kwargs: '{}'.
2024-10-26 20:48:27 DEBUG    rasa.nlu.featurizers.dense_featurizer.lm_featurizer  - Loading Tokenizer and Model for bert
2024-10-26 20:48:27 DEBUG    urllib3.connectionpool  - Starting new HTTPS connection (1): huggingface.co:443
2024-10-26 20:48:27 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/tokenizer_config.json HTTP/11" 200 0
2024-10-26 20:48:27 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/config.json HTTP/11" 200 0
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.predictions.transform.dense.bias', 'cls.predictions.transform.dense.weight', 'cls.seq_relationship.weight', 'cls.seq_relationship.bias', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.bias', 'cls.predictions.transform.LayerNorm.bias']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
2024-10-26 20:48:30 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' loading 'DIETClassifier.load' and kwargs: '{}'.
2024-10-26 20:48:30 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_DIETClassifier5' was requested for reading.
2024-10-26 20:48:30 DEBUG    rasa.utils.tensorflow.models  - Loading the model from /tmp/tmp2_g0d8el/train_DIETClassifier5/DIETClassifier.tf_model with finetune_mode=False...
2024-10-26 20:48:30 DEBUG    rasa.nlu.classifiers.diet_classifier  - You specified 'DIET' to train entities, but no entities are present in the training data. Skipping training of entities.
2024-10-26 20:48:30 DEBUG    rasa.nlu.classifiers.diet_classifier  - Following metrics will be logged during training:
2024-10-26 20:48:30 DEBUG    rasa.nlu.classifiers.diet_classifier  -   t_loss (total loss)
2024-10-26 20:48:30 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_acc (intent acc)
2024-10-26 20:48:30 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_loss (intent loss)
/home/admin/.pyenv/versions/3.10.15/lib/python3.10/random.py:370: DeprecationWarning: non-integer arguments to randrange() have been deprecated since Python 3.10 and will be removed in a subsequent version
  return self.randrange(a, b+1)
2024-10-26 20:48:43 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' loading 'EntitySynonymMapper.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_EntitySynonymMapper6' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.nlu.extractors.entity_synonyms  - Failed to load ABCMeta from model storage. Resource 'train_EntitySynonymMapper6' doesn't exist.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' loading 'ResponseSelector.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.nlu.classifiers.diet_classifier  - Failed to load ABCMeta from model storage. Resource 'train_ResponseSelector7' doesn't exist.
/home/admin/architecture-sprint-5/.venv/lib/python3.10/site-packages/rasa/utils/train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.nlu.selectors.response_selector  - Failed to load ResponseSelector from model storage. Resource 'train_ResponseSelector7' doesn't exist.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' loading 'RegexMessageHandler.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'domain_provider' loading 'DomainProvider.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'domain_provider' was requested for reading.
<frozen importlib._bootstrap>:283: DeprecationWarning: the load_module() method is deprecated and slated for removal in Python 3.12; use exec_module() instead
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' loading 'MemoizationPolicy.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_MemoizationPolicy0' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' loading 'RulePolicy.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' loading 'TEDPolicy.load' and kwargs: '{}'.
2024-10-26 20:48:43 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_TEDPolicy2' was requested for reading.
2024-10-26 20:48:43 DEBUG    rasa.utils.tensorflow.models  - Loading the model from /tmp/tmp2_g0d8el/train_TEDPolicy2/ted_policy.tf_model with finetune_mode=False...
2024-10-26 20:48:56 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' loading 'RuleOnlyDataProvider.load' and kwargs: '{}'.
2024-10-26 20:48:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'select_prediction' loading 'DefaultPolicyPredictionEnsemble.load' and kwargs: '{}'.
2024-10-26 20:48:56 INFO     root  - Rasa server is up and running.
2024-10-26 20:48:56 INFO     root  - Enabling coroutine debugging. Loop id 104574656271360.
2024-10-26 20:48:56 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'shreyas'.
2024-10-26 20:48:56 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'shreyas'.
2024-10-26 20:48:56 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'shreyas'.
2024-10-26 20:48:56 DEBUG    rasa.core.tracker_store  - Could not find tracker for conversation ID 'shreyas'.
2024-10-26 20:48:56 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2024-10-26 20:48:56 DEBUG    rasa.core.processor  - Starting a new session for conversation ID 'shreyas'.
2024-10-26 20:48:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2024-10-26 20:48:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_session_start rasa_events=[<rasa.shared.core.events.SessionStarted object at 0x7a0cc7440cd0>, ActionExecuted(action: action_listen, policy: None, confidence: None)]
2024-10-26 20:48:56 DEBUG    rasa.core.processor  - [debug    ] processor.slots.log            slot_values= session_started_metadata: None
2024-10-26 20:48:56 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7a0cc73e3040>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2024-10-26 20:48:56 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2024-10-26 20:48:57 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2024-10-26 20:48:57 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'приветствие', 'confidence': 0.9911367893218994} parse_data_text=Привет
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 4 events.
2024-10-26 20:48:57 DEBUG    rasa.core.actions.action  - Validating extracted slots:
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=0 rasa_events=[]
2024-10-26 20:48:57 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{}, {'user': {'intent': 'приветствие'}, 'prev_action': {'action_name': 'action_listen'}}]
2024-10-26 20:48:57 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'utter_greet'
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user text: Привет | previous action name: action_listen
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_greet'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_greet' based on user intent.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - Predicted next action 'utter_greet' with confidence 1.00.
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7a0cc73f1180>]
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_greet rasa_events=[BotUttered('Привет! Как я могу вам помочь?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_greet"}, 1729975737.0381067)]
2024-10-26 20:48:57 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'приветствие'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'приветствие'}, 'prev_action': {'action_name': 'utter_greet'}}]
2024-10-26 20:48:57 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
2024-10-26 20:48:57 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2024-10-26 20:48:57 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:48:57 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2024-10-26 20:48:57 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2024-10-26 20:48:57 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2024-10-26 20:48:57 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'shreyas'.
2024-10-26 20:49:40 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'shreyas'.
2024-10-26 20:49:40 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'shreyas'.
2024-10-26 20:49:40 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'shreyas'.
2024-10-26 20:49:40 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'shreyas'
2024-10-26 20:49:40 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7a0cc73e2a70>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2024-10-26 20:49:40 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2024-10-26 20:49:40 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'микросервисы', 'confidence': 0.8492256999015808} parse_data_text=Что такое микросервисы
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 9 events.
2024-10-26 20:49:40 DEBUG    rasa.core.actions.action  - Validating extracted slots:
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=0 rasa_events=[]
2024-10-26 20:49:40 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'приветствие'}, 'prev_action': {'action_name': 'utter_greet'}}, {'user': {'intent': 'микросервисы'}, 'prev_action': {'action_name': 'action_listen'}}]
2024-10-26 20:49:40 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user text: Что такое микросервисы | previous action name: action_listen
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_microservices'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_microservices' based on user intent.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - Predicted next action 'utter_microservices' with confidence 1.00.
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7a0cc73e31f0>]
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_microservices rasa_events=[BotUttered('Микросервисная архитектура — это подход к разработке, когда приложение разделяется на независимые сервисы, взаимодействующие между собой.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_microservices"}, 1729975780.3931854)]
2024-10-26 20:49:40 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e30a0>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'микросервисы'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'микросервисы'}, 'prev_action': {'action_name': 'utter_microservices'}}]
2024-10-26 20:49:40 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
2024-10-26 20:49:40 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2024-10-26 20:49:40 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:49:40 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2024-10-26 20:49:40 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2024-10-26 20:49:40 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2024-10-26 20:49:40 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'shreyas'.
2024-10-26 20:50:20 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'shreyas'.
2024-10-26 20:50:20 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'shreyas'.
2024-10-26 20:50:20 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'shreyas'.
2024-10-26 20:50:20 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'shreyas'
2024-10-26 20:50:20 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7a0cd2b54ca0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e3640>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2024-10-26 20:50:20 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2024-10-26 20:50:21 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2024-10-26 20:50:21 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'документация', 'confidence': 0.39463451504707336} parse_data_text=Документация для микросервисов
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 14 events.
2024-10-26 20:50:21 DEBUG    rasa.core.actions.action  - Validating extracted slots:
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=0 rasa_events=[]
2024-10-26 20:50:21 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e3640>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'микросервисы'}, 'prev_action': {'action_name': 'utter_microservices'}}, {'user': {'intent': 'документация'}, 'prev_action': {'action_name': 'action_listen'}}]
2024-10-26 20:50:21 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user text: Документация для микросервисов | previous action name: action_listen
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user intent: документация | previous action name: action_listen
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_documentation'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_documentation' based on user intent.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - Predicted next action 'utter_documentation' with confidence 1.00.
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7a0cd01787f0>]
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_documentation rasa_events=[BotUttered('Для документации архитектуры можно использовать схемы UML, диаграммы последовательностей и описание потоков данных.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_documentation"}, 1729975821.057277)]
2024-10-26 20:50:21 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cc73e3640>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'документация'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'документация'}, 'prev_action': {'action_name': 'utter_documentation'}}]
2024-10-26 20:50:21 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user intent: документация | previous action name: action_listen
[state 6] user intent: документация | previous action name: utter_documentation
2024-10-26 20:50:21 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2024-10-26 20:50:21 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:50:21 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2024-10-26 20:50:21 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2024-10-26 20:50:21 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2024-10-26 20:50:21 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'shreyas'.
2024-10-26 20:50:34 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'shreyas'.
2024-10-26 20:50:34 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'shreyas'.
2024-10-26 20:50:34 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'shreyas'.
2024-10-26 20:50:34 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'shreyas'
2024-10-26 20:50:34 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x7a0cd036bdf0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cd2b2a680>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2024-10-26 20:50:34 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2024-10-26 20:50:35 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2024-10-26 20:50:35 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'выбор_технологий', 'confidence': 0.4824756979942322} parse_data_text=Как выбрать стек
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 19 events.
2024-10-26 20:50:35 DEBUG    rasa.core.actions.action  - Validating extracted slots:
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=0 rasa_events=[]
2024-10-26 20:50:35 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cd2b2a680>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'документация'}, 'prev_action': {'action_name': 'utter_documentation'}}, {'user': {'intent': 'выбор_технологий'}, 'prev_action': {'action_name': 'action_listen'}}]
2024-10-26 20:50:35 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user intent: документация | previous action name: action_listen
[state 6] user intent: документация | previous action name: utter_documentation
[state 7] user text: Как выбрать стек | previous action name: action_listen
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user intent: документация | previous action name: action_listen
[state 6] user intent: документация | previous action name: utter_documentation
[state 7] user intent: выбор_технологий | previous action name: action_listen
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_choose_tech_stack'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_choose_tech_stack' based on user intent.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - Predicted next action 'utter_choose_tech_stack' with confidence 1.00.
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x7a0cd017bfd0>]
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_choose_tech_stack rasa_events=[BotUttered('Для выбора технологий нужно учитывать такие факторы, как требования проекта, масштабируемость и поддержка.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_choose_tech_stack"}, 1729975835.2406533)]
2024-10-26 20:50:35 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x7a0cd2b2a680>}, targets: ['select_prediction'] and ExecutionContext(model_id='6420e0b6c25647ce9a80aa6ddbe86008', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'выбор_технологий'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'выбор_технологий'}, 'prev_action': {'action_name': 'utter_choose_tech_stack'}}]
2024-10-26 20:50:35 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: приветствие | previous action name: action_listen
[state 2] user intent: приветствие | previous action name: utter_greet
[state 3] user intent: микросервисы | previous action name: action_listen
[state 4] user intent: микросервисы | previous action name: utter_microservices
[state 5] user intent: документация | previous action name: action_listen
[state 6] user intent: документация | previous action name: utter_documentation
[state 7] user intent: выбор_технологий | previous action name: action_listen
[state 8] user intent: выбор_технологий | previous action name: utter_choose_tech_stack
2024-10-26 20:50:35 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2024-10-26 20:50:35 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2024-10-26 20:50:35 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2024-10-26 20:50:35 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2024-10-26 20:50:35 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2024-10-26 20:50:35 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'shreyas'.
```
</details>