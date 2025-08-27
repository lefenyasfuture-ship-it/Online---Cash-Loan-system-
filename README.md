Online---Cash-Loan-system-/
├── package.json
├── src/
├── public/
└── ...

- name: Install dependencies
        run: npm ci
        working-directory: .   # root instead of ./frontend

      - name: Build project
        run: npm run build
        working-directory: .   # root instead of ./frontend

      - name: Upload build
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./build        # React build output at root
