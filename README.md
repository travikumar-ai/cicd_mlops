# cicd_mlops

## github setup:
    - Added github repo: https://github.com/travikumar-ai/cicd_mlops.git

## dvc setup:
    - Initialized dvc
    - Adding dagshub storage
      - dvc remote add origin s3://dvc
      - dvc remote modify origin endpointurl https://dagshub.com/<DagsHub-user-name>/<repo_name>.s3
      - dvc remote modify origin --local access_key_id <Token>
      - dvc remote modify origin --local secret_access_key <Token>
## Adding Data to the dvc:
    - dvc add data/data.csv
    - git add data/data.csv.dvc data/.gitignore
    - git commit -m "Data added to the repo
    - git push origin main
    - dvc push -r origin
      - origin : remote name which we want to push the data
 